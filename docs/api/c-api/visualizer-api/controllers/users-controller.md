---
id: users-controller
title: UsersController
display_sidebar: apiSidebar
sidebar_label: UsersController
hide_title: true
---

# UsersController

A controller is responsible for controlling the way that a user interacts with an MVC application. A controller contains the flow control logic for an ASP.NET MVC application. A controller determines what response to send back to a user when a user makes a browser request.

A controller is just a class

## JobsController

ProjectModel Method

```ts
    [VisualizerAPIAuthorization(perUser: false)]
    public class JobsController : VisualizerBaseController
    {
        public JobsController(DBMVisualizer.Data.VisualizerRepository repo) : base(repo) { }

        public ProjectModel Get(Guid companyId, string jobnumber)
        {
            var ret = TheRepository.GetAllProjects()
                .OrderBy(n => n.Name)
                .ToList()
                .FirstOrDefault(n => n.ProjectCompanies.Any(c => c.CompanyId == companyId && string.Equals(c.CompanyProjectJobNumber, jobnumber, StringComparison.InvariantCultureIgnoreCase)));
            if (ret != null)
                return (TheModelFactory.Create(ret));
            else
                return null;
        }
    }
```

Returns a CompanyModel
