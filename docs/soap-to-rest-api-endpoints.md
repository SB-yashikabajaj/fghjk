---
stoplight-id: 6f84jvfa552uc
---

# Mapping SOAP to REST API Operations

Global SOAP Namespace | SOAP API Method | Open API Document | Function | Operation | URL |
|--- |---|---| ---| ---| ---|
|ActivityManagementServiceClient |GetActivities | Activity Management | Get activities |	GET |	/api/activity-management/v1/activities
|ActivityManagementServiceClient | GetActivity |Activity Management | Get activity (includes status) |	GET	| /api/activity-management/v1/activities/{sid}
|ActivityManagementServiceClient | Get activity  | Activity Management | Get activity status only |	GET	| /api/activity-management/v1/activities/{sid}/status
|ActivityManagementServiceClient| CancelActivity | Activity Management | Cancel activity | POST | /api/activity-management/v1/activities/{sid}/actions/cancel
| LossAnalysisServiceClient | SubmitDetailedLossAnalysis | Detailed Loss| Submit detailed loss analysis | POST |  /api/detailed-loss/v1/detailed-loss
|LossAnalysisServiceClient | GetEventSets | Event Set Management | Get event sets | GET | /api/event-set-management/v1/event-sets
|LossAnalysisServiceClient | GetEventSets | Event Set Management | Get event set | GET | /api/event-set-management/v1/event-sets/{sid}
|ReinsuranceDataImport | SubmitImportClf | Loss Set Management | Create loss set | POST | /api/loss-set-management/v1/loss-sets
| ObjectManagementServiceClient  | GetLossModTemplates  | Loss Modification | Get loss mod templates | GET | /api/loss-modification/v1/templates
| ObjectManagementServiceClient  | GetLossModTemplate  | Loss Modification | Get loss mod templates | GET | /api/loss-modification/v1/templates/{sid}
| ReinsuranceManagementServiceClient | GetReinsurancePrograms | Reinsurance Loss | Get reinsurance analyses | GET | /api/reinsurance-analysis/v1/program-analyses 
| ReinsuranceAggregateLossAnalysisServiceClient | SubmitProgramAggregateLossAnalysis | Reinsurance Loss| Submit reinsurance loss analysis | POST | /api/reinsurance-analysis/v1/program-analyses
| ReinsuranceProgramManagementServiceClient |  GetPrograms  | Program Management | List Programs | GET  | /api/program-management/v1/programs
| ReinsuranceProgramManagementServiceClient  | CreateProgram | Program Management | Create Programs | POST | /api/program-management/v1/programs
|ExposureManagementServiceClient | Create Layer | Program Management | Create Layer | POST | /api/program-management/v1/programs/{sid}/layer
| | | Program Management | Create Scenario | POST | /api/program-management/v1/programs/{sid}/scenarios
