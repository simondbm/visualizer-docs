---
id: dbm-visualizer-dto
title: dbm-visualizer.dto.ts
sidebar_label: dbm-visualizer.dto.ts
hide_title: true
---

# dbm-visualizer.dto

## Definition

References: dbm-visualizer.enum.ts

Namespace: DBM.Visualizer.DTO


| Class                      |                     |
| ------------------------------ | ------------------- |
| CompanyGroupModel            | CompanyId, GroupId      |
| CompanyMappingModel            | Does something |
| CompanyModel                   | Companies Model       |
| CompanyPluginModel            | Company Plugins  |

```ts
export class CompanyModel {
		AdvancedSharing: boolean;
		ColorPalette: string;
		CompanyGroups: DBMVisualizer.DTO.CompanyGroupModel[];
		CompanyName: string;
		CompanyPlugins: DBMVisualizer.DTO.CompanyPluginModel[];
		CompanyProjects: DBMVisualizer.DTO.ProjectCompanyModel[];
		CompanyUsers: DBMVisualizer.DTO.CompanyUserModel[];
		CreateAccountBody: string;
		CreateAccountSubject: string;
		Description: string;
		HostUrl: string;
		Id: System.Guid;
		LogoutUrl: string;
		ResetPasswordBody: string;
		ResetPasswordSubject: string;
		RevisionsToShow: number;
		SenderAddress: string;
		SenderPassword: string;
		SenderUsername: string;
		SMTPServer: string;
	}
```