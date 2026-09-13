# SplunkOps Academy Templates

SplunkOps Academy is a centralized training application designed to support self-paced learning, user onboarding, and ongoing Splunk enablement.

This repository contains reusable Splunk Dashboard Studio templates and supporting files that organizations can customize for their own environments. Update the placeholder text, links, searches, branding, and content in each template as needed.

## Getting Started

1. Download or copy the desired JSON template.
2. Create a new dashboard in Splunk Dashboard Studio.
3. Open the dashboard source editor.
4. Replace the existing source with the template JSON.
5. Update the placeholder text, URLs, SPL, colors, and other organization-specific content.
6. Upload any required lookup files before using templates that depend on them.
7. Save and test the dashboard in your environment.

> **Tip:** Review each template for placeholder text and environment-specific settings before publishing it to users.

## Landing Page

### `soa_landing_page_template.json`

A reusable landing page for a training or enablement application. Customize the page with your application name, learning paths, helpful resources, support links, and organization branding.

## Learning Paths

### `soa_splunk_foundations_template.json`

A reusable training page for foundational Splunk learning. Point users to a training resource, then add organization-specific use cases, prompts, examples, or lessons learned that help users connect the training to their work.

### `soa_splunk4rookies_template.json`

A reusable page for promoting or retaining information from a Splunk4Rookies course, workshop, or other introductory training. Customize the objectives, duration, delivery format, course materials, and support information.

### Practical Labs

Practical lab templates are coming soon.

## References and Resources

### `soa_index_library_template.json`

A reusable library for helping users discover indexes, sourcetypes, descriptions, and keywords in their Splunk environment.

#### Lookup requirement

To render this dashboard, upload a lookup file containing the following columns:

```text
index
sourcetype
description
keywords
```

You may add, remove, or rename fields to fit your environment, but you must update the related SPL, filters, and table configuration accordingly.

Also update the dashboard's keyword buttons so the labels and token values match the terminology and data available in your environment.

### `soa_dashboard_library_template.json`

A reusable dashboard discovery page that uses Splunk's REST endpoint to list dashboards and associated metadata.

By default, the template pulls dashboards from the Search & Reporting app. Edit the SPL if you want to include dashboards from additional apps or the broader Splunk environment.

### `soa_data_model_searches_template.json`

A reusable reference page that gives users a starting point for working with Splunk data models.

This template requires the included `data_model_searches.csv` file. Upload the file as a Splunk lookup and name it exactly:

```text
data_model_searches.csv
```

The table will not render until the lookup is available to the app and accessible to the dashboard.

### `soa_ai_prompts_template.json`

A reusable prompt library that helps users get started with Splunk AI Assistant. Customize the prompts to reflect your organization's use cases, data, standards, and expected workflows.

### `soa_dashboard_standards_template.json`

A reusable page for documenting dashboard standards and best practices. Customize it with your organization's requirements for dashboard naming, metadata, design, ownership, maintenance, permissions, and review cycles.

## Support and Feedback

### `soa_contact_template.json`

A reusable Contact Us page for publishing support contacts, request procedures, office hours, training assistance, and escalation options.

### `soa_faq_template.json`

A reusable Frequently Asked Questions page. Add common questions and answers related to your Splunk environment, access process, training application, data, dashboards, and support model.

### `soa_feedback_template.json`

A reusable feedback page for collecting suggestions, reporting issues, and requesting improvements to the training application or its content.

## Supporting Materials

### `data_model_searches.csv`

The lookup file used by `soa_data_model_searches_template.json`. Upload this file to Splunk and preserve the filename unless you also update the lookup name in the dashboard SPL.

## Customization Checklist

Before publishing a template, review and update the following:

- Application and organization names
- Dashboard titles and descriptions
- Internal and external URLs
- SPL queries and app names
- Lookup filenames and permissions
- Contact and support information
- Learning objectives and instructions
- Button labels and token values
- Images, icons, colors, and branding
- Dashboard permissions and sharing settings

## File Naming

Keep the `.json` extension for Dashboard Studio source templates and the `.csv` extension for lookup files. 

## Disclaimer

These templates are intended as starting points. Test all dashboards, searches, links, permissions, and lookup dependencies in a non-production environment before making them available to users.
