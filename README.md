> [!NOTE]
> This repository has been archived in favour of https://github.com/tensorchord/cloudnative-pgvecto.rs.  
> You can safely continue using the images from this repository until you need to upgrade to a new pgvecto.rs version.

# cnpgvecto.rs
Container images for [cloudnative-pg](https://cloudnative-pg.io/) with the [pgvecto.rs](https://github.com/tensorchord/pgvecto.rs) extension installed.


> [!IMPORTANT]
> If you are using this image on an existing database, the postgres configuration needs to be 
> altered to enable the extension. You can do this by setting shared_preload_libraries in your Cluster spec:
> ```yaml
> apiVersion: postgresql.cnpg.io/v1
> kind: Cluster
> spec:
>   (...)
>   postgresql:
>     shared_preload_libraries:
>       - "vectors.so"
>   ```
