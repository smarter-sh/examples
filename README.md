# Smarter Example Manifests

[![License: AGPL v3](https://img.shields.io/badge/License-AGPL_v3-blue.svg)](https://www.gnu.org/licenses/agpl-3.0)
[![hack.d Lawrence McDaniel](https://img.shields.io/badge/hack.d-Lawrence%20McDaniel-orange.svg)](https://lawrencemcdaniel.com)

Smarter manifest examples for ChatBots and Plugins.
Read more at the [Smarter docs portal](https://platform.smarter.sh/docs/)

A Smarter Manifest is a YAML document that describes a resource that makes up part of your AI solution. It has four main parts: apiVersion, kind, spec and status. Each of these section plays a specific role in the lifecycle of your AI resources. The apiVersion identifies the Manifest document to the Smarter API. The kind identifies the type of resource being described. The spec section contains the configuration of the resource. And lastly, the status section contains read-only data about the state of resource. Here is the layout of a generic Manifest:

```yaml
apiVersion: smarter.sh/v1
kind: Chatbot
metadata:
  # Metadata about your resource goes here. These required fields are used for identifying
  # and managing your resource inside of Smarter.
  description: A human readable description of this resource. Keep it brief.
  name: MyChatbot
  version: 1.0.0
spec:
  # your specification goes here. Each kind of resource has its own spec layout
  # which you can scaffold using the Smarter CLI command `smarter manifest  -o yaml`.
  # For example: `smarter manifest chatbot -o yaml`
status:
  # read-only status about your AI resource goes here.
```

## Usage

```console
git clone https://github.com/smarter-sh/examples
smarter apply -f examples/plugins/plugin-smarter.yaml
smarter apply -f examples/chatbots/chatbot-smarter.yaml
```
