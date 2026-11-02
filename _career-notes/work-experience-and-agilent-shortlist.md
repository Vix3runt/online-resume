# Work experience review and Agilent job shortlist

Prepared on 2 November 2026. This review records the evidence and job comparison used to update the resume. The resume now includes the supported work experience, specialization, and qualified scope figures.

This file is under `_career-notes` so Jekyll does not publish it as a normal site page.

## Employment details

- Name: He ZiAng.
- Employer: Resonac HD Singapore.
- Position: System Engineer.
- Joined: 14 March 2022.
- Resume date range: March 2022 - present.
- Include development, maintenance, integration, and supported projects. Shared systems must use contribution wording where ownership is uncertain.

## Review scope and evidence limits

The review covered project folders under `/home/vix3runt/src` and `C:\Users\z115i7699\Desktop\jobs`, accessible through `/mnt/c/Users/z115i7699/Desktop/jobs`.

Evidence included repository authorship and history, implementation, project READMEs, and `ziang_mrm_2412.pptx`. Duplicate checkouts and older versions were grouped into project families. The inventory was broad, with focused inspection of the strongest candidates, rather than a line-by-line audit of every file.

Git author identities included He Ziang, HE ZIANG, HE ZIANG XMMZP, Ziang He, and Vix3runt. A repository's presence alone does not establish ownership. Historical activity dates do not establish deployment dates or continuous project assignment.

The strongest overall positioning is manufacturing software engineering across equipment data collection, engineering analysis, and quality workflows. No numerical performance improvements, cost savings, production coverage, or user counts have been established. Deployment configuration does not by itself prove a production rollout.

## Substantial project candidates

### 1. Manufacturing data logger platform

Suggested resume wording:

> Developed and maintained Python pipelines to convert sputtering equipment logs into Parquet datasets, extract process cycles, record Oracle metadata, and archive production data. Built Flask dashboards for engineering analysis and improved maintainability through modular services, database connection pooling, and processing diagnostics.

Scope includes DAT conversion through a C# DLL, pandas processing, downsampling, cycle extraction, metadata tracking, network-share inputs, and remote exports. Related folders include `data-logger-converter`, `convert_parq`, `data_logger_visualization`, `spt_logger_plot`, `ftp_plc_convert`, `spt_p28`, and `spt_vhf`.

Evidence:

- [Converter workflow](/mnt/c/Users/z115i7699/Desktop/jobs/data-logger-converter/README.md:3).
- [Visualization architecture](/mnt/c/Users/z115i7699/Desktop/jobs/data_logger_visualization/README.md:9).
- Your commit `54595b0` adds connection pooling and bounds the last-file search.
- Your commit `3c2b134` modularizes the visualization application and introduces an application factory.
- Related project history spans 2022-2026.

### 2. Guzik measurement processing and test-plan platform

Suggested resume wording:

> Developed automated Guzik measurement ingestion, data transformation, and Excel reporting workflows. Built React and Express applications backed by Oracle for test-plan configuration, target management, regeneration workflows, and measurement review.

Your presentation describes automatic file discovery, flattening raw measurement blocks, database-driven parameter mapping, golden-sample normalization, Excel reporting, test-plan configuration, and Tableau integration. It describes faster readout, but does not provide a measured improvement to quote.

Evidence:

- [API responsibilities](/home/vix3runt/src/guzik/guzik-web-api/README.md:3).
- [Python ingestion](/mnt/c/Users/z115i7699/Desktop/jobs/guzik_data_new/main.py:16).
- [Excel export](/mnt/c/Users/z115i7699/Desktop/jobs/guzik_data_new/export.py:158).
- Presentation: `C:\Users\z115i7699\Desktop\jobs\ziang_mrm_2412.pptx`.
- Your frontend commit `0bf3e40` completes a test-plan ingestion flow. Backend commit `30471e1` adds offline blue-green stack definitions.
- Data-processing history includes 2024, with web-platform development through 2026. Other contributors are present.

### 3. OMS measurement workflow and SPC integration

Suggested resume wording:

> Extended an ASP.NET/VB.NET measurement system with instrument configuration, measurement requests, acknowledgements, result uploads, and SPC integration. Implemented pKerr workflow support and contributed to FTIR reporting and operational notifications.

The system includes FTIR, Raman, uESCA, XTools, NK, TMS, and pKerr workflows. This does not imply you originally built every instrument module. Your specific extensions are supported by the commit history.

Evidence:

- [System overview and pKerr integration](/mnt/c/Users/z115i7699/Desktop/jobs/oms/oms-master/README.md:1).
- Your commit `092b49d` adds measurement forms and configurations.
- Your commit `6559056` implements the measurement request module.
- Your commit `38c5247` extends pKerr integration across request and acknowledgement workflows.
- Your commit `46e3773` adds FTIR mainbody SPC upload support.
- Related history spans 2024-2026.

### 4. VIM visual inspection modernization

Suggested resume wording:

> Developed a React/TypeScript frontend and Bun/Express API to modernize legacy visual inspection workflows, including defect tagging, inspection judgements, configurable rules, audit history, and shift reports. Prepared containerized UAT deployment with Oracle integration and controlled access to inspection images.

Describe this as modernization and UAT work unless the particular production rollout is confirmed. Multi-machine concurrency planning and a prepared deployment package are not evidence of completed production deployment.

Evidence:

- [Backend capabilities and profiles](/home/vix3runt/src/qa-vim/qa-visual-inspection-application-backend/README.md:3).
- Your backend commit `561caf7` adds shift reports, audit history, and pending work queues.
- Your backend commit `0bcc054` enforces route permissions and login limits.
- Your frontend commit `c21e1c4` adds UAT reports, the audit dashboard, and session flows.
- The new frontend and backend histories show activity in September-October 2026.

### 5. Industrial IoT and equipment health monitoring

Suggested resume wording:

> Developed and supported equipment monitoring services for pump condition, motor torque, and process parameters using Python, PostgreSQL, MQTT, and web APIs. Implemented configurable thresholds, event-driven alerts, historical data access, and monitoring interfaces.

Related folders include `pg_listener_v2`, `threshold_web`, `pi/ctb-torque-data-collector`, `pi/mqtt_master`, `pi/mqtt_broadcasting`, `CTB_V2`, `cryopump-anelva`, `cryo_monitoring`, `mms_visualization`, and `sensor_insight`.

Evidence:

- [PostgreSQL notification listener and threshold checks](/mnt/c/Users/z115i7699/Desktop/jobs/pg_listener_v2/db_help.py:52).
- [Torque collection](/mnt/c/Users/z115i7699/Desktop/jobs/pi/ctb-torque-data-collector/main.py:62).
- Your threshold web history begins in March 2022, followed by notification and reporting changes in April 2022.
- Torque collection, MQTT services, cryopump alerts, and monitoring APIs show subsequent contributions in 2023-2024.
- Multiple monitoring repositories have shared authorship. Do not claim sole ownership of the entire monitoring estate.

### 6. SPT cassette tracking and exception monitoring

Suggested resume wording:

> Developed PLC-connected services to track cassette movement and detect changes in sputtering equipment state. Implemented WebSocket event broadcasts, exception-log ingestion, Oracle records, and email summaries for operational investigation.

Evidence:

- [PLC reader setup](/mnt/c/Users/z115i7699/Desktop/jobs/spt-block/internal_test.py:375).
- [Cassette comparison and event broadcast](/mnt/c/Users/z115i7699/Desktop/jobs/spt-block/internal_test.py:565).
- Your commit `c3b4a4c` updates configuration for all lines.
- Your commit `17b6223` updates data insertion and log processing.
- Your commit `955c57a` adds email after log processing.
- Reviewed activity includes 2024. Confirm equipment-control behavior before describing this as an automatic interlock or rejection system.

### 7. Manufacturing alert migration to Microsoft Teams

Suggested resume wording:

> Contributed to migrating manufacturing alerts from Workplace messaging to Microsoft Teams through a shared Microsoft Graph service. Updated message formatting, caller configuration, and notification integrations for measurement and equipment-monitoring applications.

Evidence:

- [Migration inventory](/mnt/c/Users/z115i7699/Desktop/jobs/graph-api-middle-tier/README.md:130).
- Your commit `81850a5` changes Teams channel message formatting.
- Your commit `b5b73c5` adds a Teams caller configuration endpoint.
- OMS commits include notification integration, and a server snapshot records migrated notification source files.
- The middleware has shared authorship. Use contribution wording rather than claiming original ownership of the whole Graph service.

### 8. DX job-request workflow support

Suggested resume wording:

> Enhanced an internal job-request application with approval-routing changes, division-manager auto-approval, and email notification logic. Supported the React frontend and API integration within a shared development team.

Evidence:

- Your frontend commit `3024ca30` updates request handling and division-manager auto-approval.
- Your API commit `30b5fbb` changes approval-related logic.
- Your API commits `94fc81e`, `68f0c1c`, and `824ecbc` change finished-request notification logic.
- Later API restructuring and framework upgrades have other authors. Do not claim those changes as yours.

## Additional candidates requiring contribution confirmation

| Candidate | What the files establish | Wording boundary |
| --- | --- | --- |
| Automated IR sensor calibration | Serial-connected temperature control, sensor correction routines, calibration logging, and notifications in `auto_ir_calib`. | Confirm whether you built the calibration workflow, extended it, or supported deployment and messaging. |
| Defect evaluation and result ingestion | HDI evaluation, defect grading, radius summaries, and touchdown/grain uploads under `V5`. | Confirm your responsibility before claiming implementation. |
| PMMS data import | Excel validation and batch creation of maintenance items and machine specifications. | Confirm ownership and operational use. |
| Legacy application support | DiskMerger, HDI Defect Entry, and Thermal Decay are present. | Recorded commits mainly belong to colleagues. Include only support or maintenance you actually performed. |

## Resume selection and missing impact evidence

### Verified scope figures added on 2 November 2026

- **11 configured production lines:** `data-logger-converter/line_config.json`, under `vtc_lines`, contains unique line IDs 201-211. The pipeline reads this configuration in `main.py` and `shorten_cycle_new.py`. This establishes configured scope, not successful live processing on every line or a measured performance gain.
- **9 documented migrated alert integrations:** the migration table in `graph-api-middle-tier/README.md:134` lists nine rows marked Completed. The preceding sentence refers to seven alerts from an earlier June review; the resume count comes from the nine-row table, not that older sentence. This is documented shared-project scope, not independent live verification or sole ownership of all migrations.
- No measured before/after business impact is established. Hours saved, throughput improvements, and user counts still require supporting records or confirmation.

For general manufacturing software roles, lead with the data logger platform, Guzik, OMS, VIM, and equipment monitoring. For automation roles, move IoT and PLC tracking higher. Keep Teams migration and job-request support as shorter supporting bullets.

Before finalizing, establish production lines or machines covered, daily data volume, number of users, manual work eliminated, and any measured processing improvements. Confirm which systems reached production and your responsibility in shared projects.

## Agilent Singapore shortlist

Checked on 2 November 2026 using the supplied Singapore country filter. Agilent's public Workday feed returned 33 postings across two result pages. Multi-location roles were included when the Singapore filter matched them. The details of the nine relevant requisitions below were read from Agilent's own job endpoints and each reported `canApply: true` at the time of review.

The ranking is an assessment of fit with the reviewed work, not an employer eligibility decision. Experience in an unreviewed technology is unverified, rather than assumed absent.

### 1. Digital Solutions Engineer - Operational Applications, 4039668

[Official posting](https://agilent.wd5.myworkdayjobs.com/Agilent_Careers/job/Singapore-Yishun/Digital-Solutions-Engineer---Operational-Applications_4039668)

- Location: Singapore-Yishun. Posting date: 11 September 2026.
- Best overall match. The work concerns operational applications, inspections, approvals, frontline workflows, enterprise integration, and manufacturing productivity.
- Lead with VIM, OMS, Guzik, and DX job-request support. Your React applications, REST APIs, manufacturing workflows, and computer science degree address the core profile.
- Preferred areas to discuss honestly: mobile and cross-platform development, offline-first synchronization, cloud-native applications, and AI-enabled experiences. The old internship mentions React Native, but recent professional mobile delivery is not established.
- The posting welcomes multiple career stages rather than specifying a fixed minimum number of years.

### 2. Digital Solutions Engineer - Platform Services, 4039669 and 4039991

[Official posting 4039669](https://agilent.wd5.myworkdayjobs.com/Agilent_Careers/job/Singapore-Yishun/Digital-Solutions-Engineer---Platform-Services_4039669)

[Official posting 4039991](https://agilent.wd5.myworkdayjobs.com/Agilent_Careers/job/Singapore-Yishun/Digital-Solutions-Engineer---Platform-Services_4039991)

- Location: Singapore-Yishun. Posting dates: 13 October and 14 September 2026 respectively.
- Strong backend and integration match. The role covers services, APIs, enterprise integration, relational databases, and connected manufacturing systems.
- Lead with Guzik and VIM APIs, OMS/SPC integration, Teams integration, PostgreSQL events, MQTT services, Docker configuration, and deployment preparation.
- Core strengths include Python, backend application work, APIs, and manufacturing domain knowledge. Cloud concepts and distributed architecture are part of the required profile. Azure or AWS delivery, Kubernetes, and large-scale messaging are areas to validate or develop.
- Both postings welcome multiple career stages and have closely overlapping descriptions. They are separate requisitions, not assumed separate opportunities with different technical requirements.
- The details list occasional travel for 4039669 and no travel for 4039991. Confirm the relevant team and requisition with the recruiter.

### 3. Digital Solutions Engineer - Application Experience, 4039670

[Official posting](https://agilent.wd5.myworkdayjobs.com/Agilent_Careers/job/Singapore-Yishun/Digital-Solutions-Engineer---Application-Experience_4039670)

- Location: Singapore-Yishun. Posting date: 18 September 2026.
- Strong match for manufacturing interfaces and workflows. Lead with VIM, Guzik, OMS, and visualization dashboards.
- The title says Application Experience, but its description refers to Operational Applications and closely overlaps 4039668. Treat the apparent distinction cautiously.
- Your React and TypeScript work supports the application-development profile. Recent mobile delivery, offline synchronization, accessibility practice, and SAP or MES integrations are not established by the review.
- This belongs in the same first-priority application group as Operational Applications and Platform Services. It ranks third here because of overlap, not because it is a poor fit.

### 4. Global Operations Data Engineer, 4039671

[Official posting](https://agilent.wd5.myworkdayjobs.com/Agilent_Careers/job/Singapore-Yishun/Global-Operations-Data-Engineer_4039671)

- Location: Singapore-Yishun. Posting date: 11 September 2026.
- Strong overlap with Python and SQL pipelines, manufacturing data integration, Parquet conversion, metadata tracking, and equipment telemetry.
- Lead with the data logger platform, Guzik ingestion, FTP/PLC conversion, and equipment data services.
- A larger technology gap than the application roles: scalable cloud-based data solutions appear in the required profile. Azure, AWS, Databricks, Fabric, lakehouses, formal governance, and lineage are not established by the inspected work.
- A worthwhile application if you want to specialize in data engineering, with those gaps stated honestly.

## Lower-priority Agilent roles

| Role | Assessment |
| --- | --- |
| [Global Operations Data Architect, 4039672](https://agilent.wd5.myworkdayjobs.com/Agilent_Careers/job/Singapore-Yishun/Global-Operations-Data-Architect_4039672-1) | Stretch. Relevant integration and data-engineering work, but enterprise-wide architecture, governance, modeling standards, and cloud data platforms need stronger evidence. The posting welcomes multiple career stages, so this is a scope gap rather than an assumed years-of-experience rejection. |
| [AI and Data Scientist - Smart Manufacturing, 4039673](https://agilent.wd5.myworkdayjobs.com/Agilent_Careers/job/Singapore-Yishun/AI---Data-Scientist---Smart-Manufacturing_4039673-1) | Stretch. Manufacturing data and Python are relevant, but the review does not establish applied ML or statistical-model delivery. AI coding-tool use does not establish model-development experience. |
| [Simulation and Digital Twin Engineer, 4040376](https://agilent.wd5.myworkdayjobs.com/Agilent_Careers/job/Singapore-Yishun/Simulation---Digital-Twin-Engineer_4040376) | Lower fit. Requires at least five years of relevant experience plus simulation, robotics, digital-twin, or automation software and physical modeling knowledge. Your current company tenure is about four years and seven months; relevant simulation experience is not established. |
| [MSAT System Engineer, 4038755](https://agilent.wd5.myworkdayjobs.com/Agilent_Careers/job/Singapore-Yishun/Manufacturing-Science-and-Technology--MSAT--System-Engineer_4038755-1) | Low fit despite the similar title. Requires eight or more years of comparable experience and focuses on mechanical and mechatronic instrument design, CAD, and PCBA qualification. |

## Resume emphasis for the shortlisted roles

- Operational Applications and Application Experience: put VIM, OMS, and Guzik first. Emphasize translating factory workflows into usable applications, integrating APIs, and supporting operators and engineers.
- Platform Services: put APIs, system integration, database-backed services, authentication, event handling, diagnostics, and deployment work first.
- Data Engineer: put automated ingestion, transformation, process-cycle extraction, Parquet, SQL, metadata, and failure handling first.
- Use the official System Engineer title. A summary can describe the specialization as manufacturing software, data pipelines, and industrial IoT.
- Do not add cloud, SAP, MES, Kubernetes, production AI, or measured business results unless supported by actual experience.

No applications were submitted. The resume data and the one-page PDF have been updated. Job availability reflects the check on 2 November 2026.
