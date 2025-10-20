<!-- Profile Header -->
<h1 align="center">👋 Hi, I'm Mahmoud Osman</h1>
<h3 align="center">Full-Stack Developer | Building scalable web apps with React, Node.js, and Express</h3>

<p align="center">
  <a href="https://github.com/mahmoudahmadosman">
    <img src="https://komarev.com/ghpvc/?username=mahmoudahmadosman&label=Profile%20views&color=1E90FF&style=flat-square" alt="Profile views" />
  </a>
  <a href="https://github.com/mahmoudahmadosman?tab=followers">
    <img src="https://img.shields.io/github/followers/mahmoudahmadosman?label=Followers&style=flat-square&color=brightgreen" alt="GitHub followers" />
  </a>
  <a href="mailto:Ibrahim.gaabow1989@gmail.com">
    <img src="https://img.shields.io/badge/Email-Contact%20Me-blue?style=flat-square&logo=gmail" alt="Email Badge"/>
  </a>
</p>

---

### 🧠 About Me
- 🔭 I’m currently working on **MERN Stack Projects**  
- 🌱 Learning **TypeScript, Next.js, and Express.js automation**  
- 💡 Passionate about **building scalable and efficient backend systems**  

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
