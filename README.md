# Shinje

Shinje, Lord of Death: weighs every deed before passing judgment.

Shinje is a risk-adaptive access control (RAdAC) system. It weighs the risk of each request before judging it. User and entity behavior analytics (UEBA) is one of its signals. UEBA keeps a baseline of normal activity for users and for entities such as hosts, services and API clients, so unusual activity stands out. WIP.

## RAdAC

Risk-adaptive access control decides each request when it is made. It scores the request's risk from signals about the subject, the resource and the context, such as the subject's recent activity, the resource's sensitivity, the time of day and the network the request comes from. A policy maps the score to a decision: allow, deny, or require stronger proof, such as a second factor. A permission check asks whether the subject may perform the action. RAdAC also asks whether this request, made now, is safe to grant.

## UEBA

User and entity behavior analytics learns what normal activity looks like for each user and for each entity, such as a host, a service or an API client. It builds the baseline from past activity: when an account signs in, from where, what it reads and how much. It scores new activity by how far it departs from that baseline. A sign-in at an unusual hour, a read of data the account has never touched, or a sudden burst of requests each raise the score. UEBA detects and reports. It does not decide access. In Shinje, its score is one of the signals the RAdAC policy weighs.
