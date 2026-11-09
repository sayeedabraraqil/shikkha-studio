# Shikkha Studio — SSC Class 10 Classroom

A simple static website for publishing your own curated YouTube class links.

## Files
- `index.html` — complete website UI and player
- `classes.json` — the only file you need to edit to add or remove classes
- `vercel.json` — static deployment configuration

## Add a class
Open `classes.json` and add an object inside the `classes` array:

```json
{
  "id": "phy-002",
  "title": "Work, Energy and Power",
  "subject": "Physics",
  "chapter": "Chapter 3 · Work and Energy",
  "lecture": 2,
  "youtubeUrl": "https://www.youtube.com/watch?v=YOUR_VIDEO_ID",
  "description": "A short description of this lesson."
}
```

Important:
- Use a unique `id` for every class.
- `subject` should match one of the subject names in the `subjects` array.
- Use a real YouTube watch, youtu.be, Shorts, Live or embed URL.
- Keep valid JSON syntax: commas between objects, but no comma after the last object.
- Replace or remove the three example entries before publishing.

## Deploy to Vercel
1. Extract this ZIP.
2. Create a GitHub repository and upload all three files, keeping them in the project root.
3. In Vercel, choose **Add New → Project**, import the repository.
4. Use the default static deployment settings. No build command is required.
5. Deploy. Your public Vercel URL is the link you share with students.
6. Whenever you edit `classes.json`, commit and push to GitHub. Vercel automatically redeploys the site.

## YouTube player note
The website uses the YouTube privacy-enhanced embed host and `rel=0`. YouTube controls its own player UI and may still show certain overlays or branding. `rel=0` limits related videos to the same channel; it does not guarantee that every YouTube overlay can be removed. When the player reports that the class has ended, the site displays its own completion cover instead of loading another class.

## No backend
There is no database, login, admin dashboard, or user-submitted content. Visitors can only view the class links you publish in `classes.json`.
