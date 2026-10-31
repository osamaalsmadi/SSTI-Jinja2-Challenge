# Jinja2 Template Injection Lab

Educational Jinja2 SSTI assessment, remediation notes, and a containerized lab.

**Python · Flask · Jinja2 · Docker**

## Learning focus

The boundary between user-controlled text and executable server templates.

## Repository guide

| Resource | Location |
| --- | --- |
| Assessment | [professional_training/module01/ex00/Readme.md](professional_training/module01/ex00/Readme.md) |
| Remediation | [professional_training/module01/ex00/Fix.md](professional_training/module01/ex00/Fix.md) |
| Compose configuration | [professional_training/module01/ex00/pro_00/docker-compose.yml](professional_training/module01/ex00/pro_00/docker-compose.yml) |

## Inspect the lab

1. Read the assessment and remediation notes together.
2. Inspect the Dockerfile and Compose configuration before running the application.
3. Use an isolated local environment for authorized training. The supplied Compose file publishes a host port; it is not a production deployment configuration.
4. Record observations and compare them with the mitigation notes.

## Setup requirements

Docker with Compose is required for the supplied container configuration. The lab directory is `professional_training/module01/ex00/pro_00`.

Container builds and vulnerability demonstrations have not been revalidated as part of this documentation update.

## Additional material

The separate `CSS-Visual-Presentation/` directory contains frontend exercises and is independent of the security lab.

---

Part of [Osama Alsmadi’s project portfolio](https://github.com/osamaalsmadi).
