# Pritom Chowdhury — Live Portfolio Feature

This repository contains one working dynamic feature for the FlyRank **Make It Do Something** assignment: a portfolio contact form that sends a real message through the free FormSubmit.co form backend.

## Live demo

After GitHub Pages is enabled, the site is available at:

`https://pritam6304.github.io/rag-internship-project/`

## What the feature does

A visitor enters their name, email, and project brief. The browser sends the form as an HTTPS `POST` request to FormSubmit.co. FormSubmit forwards the message to `coderpritom03@gmail.com`. The service then redirects the visitor to `thank-you.html`, which confirms the submission.

This is intentionally one complete feature rather than several half-built features.

## Plain-English data flow

1. The visitor fills out the form in `index.html`.
2. The browser validates the required fields and email format.
3. The form sends the values over HTTPS to FormSubmit.co using a normal HTML `POST`.
4. FormSubmit acts as the small backend: it receives the fields, applies the subject line, and forwards the message to the configured inbox.
5. FormSubmit redirects the sender to `thank-you.html` using the `_next` field.
6. The hidden honeypot field helps discard simple bot submissions.

## Why this is free-tier friendly

The page is static and hosted on free GitHub Pages. The form handling uses FormSubmit.co's free endpoint, so no server or paid hosting is required for this small portfolio feature.

## Real test

Use a real name, a reachable email address, and a short message at the live URL. Submit the form. Evidence should show both:

- the browser reaching the `thank-you.html` confirmation page; and
- the forwarded message arriving in `coderpritom03@gmail.com`.

If FormSubmit asks for one-time activation, click the activation link delivered to the inbox; subsequent submissions will work normally.

## Files

- `index.html` — portfolio page and working form.
- `thank-you.html` — post-submit confirmation page.
- `README.md` — architecture and plain-English explanation.
