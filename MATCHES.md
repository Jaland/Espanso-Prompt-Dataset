# Complete Espanso Matches Reference

This document contains all available matches organized by category.

## 📊 Summary

| Category | File | Total Matches |
|----------|------|---------------|
| [Commit Messages](#commit-messages) | `prompts/coding/commit-messages.yaml` | 6 |
| [Development](#development) | `prompts/coding/development.yaml` | 7 |
| [AI/Fantasy Football](#ai-fantasy-football) | `prompts/ai/fantasy-football-prompts.yaml` | 2 |
| [AI/OpenShift](#ai-openshift) | `prompts/ai/openshift.yaml` | 1 |
| [Global Variables](#global-variables) | `prompts/global-variables.yaml` | 9 |
| [Personal Common](#personal-common) | `prompts/personal/common.yaml` | 1 |
| [Email/Productivity](#email-productivity) | `prompts/productivity/email.yaml` | 6 |
| [Professional/Admin](#professional-admin) | `prompts/professional/admin.yaml` | 1 |
| [Text Expansion](#text-expansion) | `prompts/text-expansion/abbreviations.yaml` | 21 |
| **Total** |  | **54** |

---

## Commit Messages
*File: `prompts/coding/commit-messages.yaml`*

| Trigger | Description | Output |
|---------|-------------|---------|
| `:commit-fix` | Bug fix commit (PATCH) | `fix: ` |
| `:commit-feat` | New feature commit (MINOR) | `feat: ` |
| `:commit-bc` | Breaking change commit (MAJOR) | `feat!: ` with BREAKING CHANGE footer |
| `:commit-docs` | Documentation changes | `docs: ` |
| `:commit-refactor` | Code refactoring | `refactor: ` |
| `:commit-chore` | Maintenance tasks | `chore: ` |

## Development
*File: `prompts/coding/development.yaml`*

| Trigger | Description | Output |
|---------|-------------|---------|
| `:pydef` | Python function template | Complete function with docstring |
| `:jsfunction` | JavaScript function template | Complete function with comments |
| `:gitfix` | Git fix commit template | `fix: [description]` |
| `:gitfeat` | Git feature commit template | `feat: [description]` |
| `:gitdocs` | Git docs commit template | `docs: [description]` |
| `:tryexcept` | Python try/except block | Complete try/except structure |
| `:ifmain` | Python main guard | `if __name__ == "__main__":` block |

## AI/Fantasy Football
*File: `prompts/ai/fantasy-football-prompts.yaml`*

| Trigger | Description | Output |
|---------|-------------|---------|
| `:ai-ff-complex-ad` | Complex AI ad generation prompt | Detailed photorealistic banner template |
| `:ai-ff-ad` | Simple AI ad generation prompt | Basic banner template with 3:1 ratio |

## AI/OpenShift
*File: `prompts/ai/openshift.yaml`*

| Trigger | Description | Output |
|---------|-------------|---------|
| `:ai-rhocp` | Red Hat OpenShift question template | Structured troubleshooting format |

## Global Variables
*File: `prompts/global-variables.yaml`*

| Trigger | Description | Output |
|---------|-------------|---------|
| `:myname` | Your full name | Jamie Land |
| `:myshortname` | Your short name | Jamie |
| `:myemail` | Your email address | hokie10@gmail.com |
| `:today` | Current date | YYYY-MM-DD format |
| `:now` | Current time | HH:MM format |
| `:datetime` | Current date and time | YYYY-MM-DD HH:MM format |
| `:regards` | Best regards signature | "Best regards,\nJamie Land" |
| `:sincerely` | Sincerely signature | "Sincerely yours,\nJamie Land" |
| `:signature` | Email signature | Name and email |

## Personal Common
*File: `prompts/personal/common.yaml`*

| Trigger | Description | Output |
|---------|-------------|---------|
| `:thanks` | Thank you message | "Thank you for your time and consideration." |

## Email/Productivity
*File: `prompts/productivity/email.yaml`*

| Trigger | Description | Output |
|---------|-------------|---------|
| `:emailmeet` | Meeting request template | Complete meeting invitation email |
| `:emailfollow` | Follow-up email template | Professional follow-up email |
| `:emailthank` | Thank you email template | Gratitude email template |
| `:ack` | Quick acknowledgment | "Thanks for letting me know..." |
| `:schedule` | Calendar confirmation | "I've added this to my calendar..." |
| `:needinfo` | Request for information | "Could you please provide more details..." |

## Professional/Admin
*File: `prompts/professional/admin.yaml`*

| Trigger | Description | Output |
|---------|-------------|---------|
| `:meetingnotes` | Meeting notes template | Complete meeting notes structure |

## Text Expansion
*File: `prompts/text-expansion/abbreviations.yaml`*

| Trigger | Description | Output |
|---------|-------------|---------|
| `:btw` | By the way | "by the way" |
| `:fyi` | For your information | "for your information" |
| `:imo` | In my opinion | "in my opinion" |
| `:imho` | In my humble opinion | "in my humble opinion" |
| `:asap` | As soon as possible | "as soon as possible" |
| `:eod` | End of day | "end of day" |
| `:eta` | Estimated time of arrival | "estimated time of arrival" |
| `:tbd` | To be determined | "to be determined" |
| `:tbc` | To be confirmed | "to be confirmed" |
| `:wfh` | Work from home | "work from home" |
| `:api` | API expansion | "Application Programming Interface" |
| `:url` | URL expansion | "Uniform Resource Locator" |
| `:sql` | SQL expansion | "Structured Query Language" |
| `:css` | CSS expansion | "Cascading Style Sheets" |
| `:html` | HTML expansion | "HyperText Markup Language" |
| `:json` | JSON expansion | "JavaScript Object Notation" |
| `:xml` | XML expansion | "eXtensible Markup Language" |
| `teh` | Typo correction | "the" |
| `adn` | Typo correction | "and" |
| `taht` | Typo correction | "that" |
| `wich` | Typo correction | "which" |
| `recieve` | Typo correction | "receive" |
| `gti` | Typo correction | "git" |

---

## 🎯 Usage Tips

- **Triggers with colons** (`:`) are intentional expansions you type
- **Triggers without colons** (like `teh`) are automatic typo corrections
- **Variables in brackets** like `[name]` or `[description]` are placeholders for you to fill in
- **Global variables** like `{{myname}}` are automatically replaced with your values
- **Multi-line expansions** preserve formatting and indentation

## 🔄 Quick Reference by Use Case

### 💻 **Coding & Development**
`:commit-fix`, `:commit-feat`, `:commit-bc`, `:pydef`, `:jsfunction`, `:tryexcept`, `:ifmain`

### 📧 **Email & Communication**  
`:emailmeet`, `:emailfollow`, `:emailthank`, `:ack`, `:regards`, `:signature`

### 📅 **Time & Personal Info**
`:today`, `:now`, `:datetime`, `:myname`, `:myemail`

### 📝 **Documentation & Notes**
`:meetingnotes`, `:commit-docs`

### 🔤 **Text Shortcuts & Corrections**
`:btw`, `:fyi`, `:asap`, `:api`, `teh`, `gti`

### 🤖 **AI Prompts**
`:ai-ff-ad`, `:ai-rhocp`

---

*Last updated: Generated automatically from prompt files*
