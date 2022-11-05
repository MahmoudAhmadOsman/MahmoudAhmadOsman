 <h3 align="left">Hi 👋, I'm Mahmoud Osman</h3>

<p align="left"> <img src="https://komarev.com/ghpvc/?username=mahmoudahmadosman&label=Profile%20views&color=0e75b6&style=flat" alt="mahmoudahmadosman" /> </p>
 
 
```bash
<section class="course-list-page" layout:fragment="content">
    <div class="container">
        <!-- Show success alert when a course is updated-->
        <div class="alert alert-info" role="alert" th:text="${successUpdate}" th:if="${successUpdate}"></div>
        <div class="alert alert-danger" role="alert" th:text="${deleteSuccess}" th:if="${deleteSuccess}"></div>
        <div class="row">
            <div class="col-md-10">
                <h1 class="text-info">List of Courses</h1>
                <hr>
            </div>
            <div class="col-md-2">
                <a href="/courses/add" class="btn btn-success">Add Course</a>
            </div>
        </div>
        <div class="row">
            <div class="col-md-3" th:each="course, stat : ${courses}">
                <div class="thumbnail">
                    <img src="https://source.unsplash.com/1600x900/?code" alt="course image">
                    <div class="caption">
                        <h3><a th:href="@{/courses/details/{id}(id=${course.id})}" th:text="${course.title}"></a>
                            <span class="badge" th:text="${stat.index + 1}">1</span></h3>
                        <!-- <p><b>Instructor: </b>[[${course.instructor}]]</p>-->
                        <p><b>Credits: </b> [[${course.credit}]]</p>
                        <p> [[${course.description}]]</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</section>

```bash
