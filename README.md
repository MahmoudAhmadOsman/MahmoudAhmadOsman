 <h3 align="left">Hi 👋, I'm Mahmoud Osman</h3>

<p align="left"> <img src="https://komarev.com/ghpvc/?username=mahmoudahmadosman&label=Profile%20views&color=0e75b6&style=flat" alt="mahmoudahmadosman" /> </p>
 
 
```bash
@Override
    protected void doPost(HttpServletRequest req, HttpServletResponse resp) throws ServletException, IOException {

        try {
            NewRequestReimbursementType request = mapper.readValue(req.getInputStream(), NewRequestReimbursementType.class);
            ReimbursementType createdReimbursementType = reimbursementTypeService.createReimbursementType(request);
            resp.setContentType("application/json");
            resp.setStatus(200);
            resp.getWriter().write(mapper.writeValueAsString(createdReimbursementType.getType_id())); 
            resp.getWriter().write(mapper.writeValueAsString(createdReimbursementType.getType_id()));
        } catch (InvalidSQLException e) {
            resp.setStatus(404);
            resp.getWriter().write(mapper.writeValueAsString(e.getMessage()));
        } catch (ResourceConflictException e) {
            resp.setStatus(409);
        }

    }

```


```
#### Recent Projects Link
```
- Projects: [Links](https://recent-projects.vercel.app/) click to visit.

