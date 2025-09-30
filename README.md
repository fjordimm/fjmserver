
# fjmserver

## Usage

Before building for development or production, do:

```
npm install
```

### Development

To start, simply do:

```
npm run dev
```

You will be able to test out the website at `http://localhost:3000`.

To exit, just press `^C`.

### Production

To build and start, simply do:

```
docker compose up
```

If there are problems, try:

```
docker compose up --build
```

You will be able to test out the website at `http://localhost:3000`.

To exit, just press `^C`.

To stop daemons, do:
```
docker compose down
```
