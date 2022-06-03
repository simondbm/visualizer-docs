---
id: data-wrapper
title: Data Wrapper
display_sidebar: apiSidebar
sidebar_label: Data Wrapper
hide_title: true
---

# Data Wrapper

To add a Model, click the Projects and Models button to open the Projects and Models Management Window.

## GetCompanyAsync

```ts
        public static async Task<DBMVisualizer.DTO.CompanyModel> GetCompanyAsync(Guid companyId)
        {
            var apiUrl = "api/companies/" + companyId;
            var data = await Get<DBMVisualizer.DTO.CompanyModel>(apiUrl);
            return data;
        }
```

Returns a CompanyModel
