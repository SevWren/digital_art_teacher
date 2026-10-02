# R5 Retrieval Failures
# Agent: R5
# Date: 2026-10-02

## Summary of Failed / Degraded Retrievals

### URL 4: https://gurneyjourney.blogspot.com/2010/06/stages-of-painting.html
- Status: COMPLETE FAILURE — page no longer exists on Blogspot
- All 8 methods exhausted. No Wayback archive exists for this URL.
- Blogspot blog has moved to Substack. Specific old posts are deleted.

### URL 5: https://gurneyjourney.blogspot.com/2009/02/value-study-first.html
- Status: COMPLETE FAILURE — page no longer exists on Blogspot
- All 8 methods exhausted. No Wayback archive exists for this URL.
- Same issue as URL 4.

### URL 9: https://www.svslearn.com/blog
- Status: COMPLETE FAILURE — page returns 404 "page not found"
- Wayback CDX API confirmed no archive snapshot available.
- SVSLearn blog may have been restructured or removed.

### URL 10: https://www.svslearn.com/blog/digital-illustration-workflow
- Status: COMPLETE FAILURE — page returns 404 "page not found"
- Wayback CDX API confirmed no archive snapshot available.
- Specific article appears deleted or moved.

### URL 13: https://www.pencilkings.com/digital-painting-workflow/
- Status: COMPLETE FAILURE — page returns 404 "page not found"
- Wayback CDX API returned empty archived_snapshots.
- Pencil Kings appears to have reorganized their content.

### URL 14: https://www.drawingfromscratch.com/
- Status: PARTIAL FAILURE — site is live but in maintenance mode
- Returns only a maintenance page: "Site will be available soon."
- No content accessible via any method.

### URL 15: https://www.illustrationage.com/
- Status: PARTIAL FAILURE — site uses JavaScript bot detection
- Wayback CDX found a snapshot (20260930013951) but Wayback itself blocked the request as suspected bot traffic.
- Direct access blocked by Cloudflare/JS challenge.

## Cross-cutting Issue
- WebFetch tool (Method 1): Failed for ALL URLs with internal AWS Bedrock auth error:
  "User: arn:aws:iam::841162713753:user/bedrock-sonnet-invoke is not authorized to perform: bedrock:InvokeModelWithResponseStream"
  This is an environment-level issue, not a per-URL issue. All retrievals fell back to curl/wget/python methods.
