---
description: A portrait for a team member, with image, link, name, and role
---

# Portrait

\
​👁 [PREVIEW](https://greenelab.github.io/lab-website-template/testbed#portrait)​

Typically you'd use this with the [list](https://greene-lab.gitbook.io/lab-website-template-docs/basics/components/list) component, which would automatically read from `members` and pass this component the parameters. But you can also use it stand-alone to manually display individual members:

```liquid
{%
    include portrait.html
    lookup="tim-member"
    style="small"
%}
```



| Parameter     | Description                                                                                                                                                                                      |
| ------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `lookup`      | Lookup member details from `members` by filename, without the `.md` extension.                                                                                                                   |
| `style`       | Visual style of the portrait. Set to `small` to make it a bit smaller, or set to `tiny` to make it very small and horizontal layout.                                                             |
| `name` / etc. | The same parameters outlined in [team members](https://greene-lab.gitbook.io/lab-website-template-docs/basics/team-members). Retrieved from lookup, or passed automatically from list component. |
