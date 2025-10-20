<!-- Profile Header -->
<h1 align="center">👋 Hi, I'm Mahmoud Osman</h1>
<h3 align="center">Full-Stack Developer | Building scalable web apps with React, Node.js, Express, Java, Springboot, JPA, SQL & Angular</h3>

<p align="center">
  <a href="https://github.com/mahmoudahmadosman">
    <img src="https://komarev.com/ghpvc/?username=mahmoudahmadosman&label=Profile%20views&color=1E90FF&style=flat-square" alt="Profile views" />
  </a>
  <a href="https://github.com/mahmoudahmadosman?tab=followers">
    <img src="https://img.shields.io/github/followers/mahmoudahmadosman?label=Followers&style=flat-square&color=brightgreen" alt="GitHub followers" />
  </a>
  <a href="mailto:osman.techy@gmail.com">
    <img src="https://img.shields.io/badge/Email-Contact%20Me-blue?style=flat-square&logo=gmail" alt="Email Badge"/>
  </a>
</p>

---

### 🧠 About Me
I'm a passionate **Full-Stack Developer** with a deep love for creating innovative web solutions that make a real impact.  
My journey in software development spans over **7+ years of experience**, during which I've honed my skills across the entire technology stack — from front-end design to backend architecture and deployment.

 

---

### 💻 Featured Code Snippet
Here’s a sample of one of my backend implementations — clean, efficient, and production-ready.

```java
@Override
protected void doPost(HttpServletRequest req, HttpServletResponse resp) throws ServletException, IOException {
    try {
        NewRequestReimbursementType request = mapper.readValue(req.getInputStream(), NewRequestReimbursementType.class);
        ReimbursementType createdReimbursementType = reimbursementTypeService.createReimbursementType(request);
        resp.setContentType("application/json");
        resp.setStatus(200);
        resp.getWriter().write(mapper.writeValueAsString(createdReimbursementType.getType_id()));
    } catch (InvalidSQLException e) {
        resp.setStatus(404);
        resp.getWriter().write(mapper.writeValueAsString(e.getMessage()));
    } catch (ResourceConflictException e) {
        resp.setStatus(409);
    }
}
