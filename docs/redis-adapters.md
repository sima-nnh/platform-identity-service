# Redis in the adapters layer

Caching for posts goes through **adapter** types (`postCachingRepository` / `postCachingRepositoryImpl`) that wrap the Redis client injected from the outer infrastructure layer. Use cases depend on the port, not on Redis APIs directly—this matches the clean architecture dependency rule and keeps **Redis usage** easy to swap or mock in tests.
