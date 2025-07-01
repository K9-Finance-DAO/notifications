# notifications

### Notifications Schema

Edit `notifications.json` with an array of messages:

```json
{
  "messages": [...]
}
```

Messages should be objects matching this interface:

```ts
interface GlobalMessage {
  id: string;
  type: 'info' | 'warning' | 'error' | 'success';
  content: string;
  startDate?: string;
  endDate?: string;
  dismissible: boolean;
  priority: number;
  link?: {
    text: string;
    url: string;
  };
}
```
