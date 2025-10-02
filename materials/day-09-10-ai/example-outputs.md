# Example Outputs (for validation)

Azure AI Search (sample query results):
```json
{
  "value": [
    { "@search.score": 1.0, "id": "1", "title": "Contoso Super Blender" },
    { "@search.score": 0.7, "id": "3", "title": "City Park Renovation" }
  ],
  "@odata.count": 2
}
```

AI Vision (sample for happy-dog.jpg):
```json
{
  "image": "happy-dog.jpg",
  "tags": ["dog", "animal", "outdoor"],
  "caption": "A happy dog running outside"
}
```
