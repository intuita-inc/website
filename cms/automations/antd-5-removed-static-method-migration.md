---
created-on: 2023-12-22T11:32:17.776Z
f_long-description: >-
  ## Description
  

  Replace message.warn with message.warning.
  Replace notification.close with notification.destroy.
  

  
  ### Before
  
  ```TypeScript
  
  import { message, notification } from 'antd';
  
  const App = () => {
    const [messageApi, contextHolder] = message.useMessage();
    const onClick1 = () => {
     message.warn();
  
    }
    const onClick2 = () => {
     messageApi.warn();
    };
  
    const [notificationApi] = notification.useNotification();
    const onClick3 = () => {
     notification.close();
    }
    const onClick4 = () => {
     notificationApi.close();
    };
  
    return <>{contextHolder}</>;
  };
  
  
  ```
  
  ### After
  
  ```TypeScript
  
  import { message, notification } from 'antd';
  
  const App = () => {
    const [messageApi, contextHolder] = message.useMessage();
    const onClick1 = () => {
     message.warning();
    }
    const onClick2 = () => {
     messageApi.warning();
    };
  
    const [notificationApi] = notification.useNotification();
    const onClick3 = () => {
     notification.destroy();
    }
    const onClick4 = () => {
     notificationApi.destroy();
    };
  
    return <>{contextHolder}</>;
  };
  
  ```
f_github-link: https://github.com/intuita-inc/codemod-registry/tree/main/codemods/antd/5/removed-static-method-migration
f_vs-code-link: vscode://intuita.intuita-vscode-extension/showCodemod?chd=kGFeVKZNWhdp1Al8BJ03ZYs_T-s
f_cli-command: intuita antd/5/removed-static-method-migration
f_framework: cms/framework/antd.md
f_applicability-criteria: Ant Design >= 5.0.0
f_verified-codemod: true
f_author: cms/authors/intuita.md
layout: "[automations].html"
slug: antd-5-removed-static-method-migration
title: Antd V5 - Removed Static Method Migration
f_slug-name: antd-5-removed-static-method-migration
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Assistive
f_estimated-time-saving: Up to 1 minutes/occurrence
tags: automations
updated-on: 2023-12-22T11:32:17.777Z
published-on: 2023-12-22T11:32:17.777Z
seo:
  title: Antd V5 - Removed Static Method Migration | Intuita Automations
  og:title: Antd V5 - Removed Static Method Migration | Intuita Automations
  twitter:title: Antd V5 - Removed Static Method Migration | Intuita Automations
  description: Replace message.warn with message.warning.
  twitter:card: Replace message.warn with message.warning.
---