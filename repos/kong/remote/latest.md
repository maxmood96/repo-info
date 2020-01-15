## `kong:latest`

```console
$ docker pull kong@sha256:a88c35cb8e7807966b6aaf1b41da3809b4b2c86ae50f7d036f90cb2aa747133a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:latest` - linux; amd64

```console
$ docker pull kong@sha256:e0740a0092bcd9fa57803ba815918f3622f6b7862c38b6c7db9e1b76bc4c4893
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44116155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:047d4996f6afd73e35643ce1250fe4aa6504fa1e8e190942a0f154075af6420f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 21 Oct 2019 17:21:42 GMT
ADD file:fe1f09249227e2da2089afb4d07e16cbf832eeb804120074acd2b8192876cd28 in / 
# Mon, 21 Oct 2019 17:21:42 GMT
CMD ["/bin/sh"]
# Mon, 21 Oct 2019 18:58:07 GMT
LABEL maintainer=Kong Core Team <team-core@konghq.com>
# Tue, 14 Jan 2020 22:20:00 GMT
ENV KONG_VERSION=1.4.3
# Tue, 14 Jan 2020 22:20:00 GMT
ENV KONG_SHA256=419d4e3d19f2d5c35ec6367e736b0d5509be4a7577d203008514a90f8dd5fdf1
# Tue, 14 Jan 2020 22:20:10 GMT
RUN adduser -Su 1337 kong 	&& mkdir -p "/usr/local/kong" 	&& apk add --no-cache --virtual .build-deps curl wget tar ca-certificates 	&& apk add --no-cache libgcc openssl pcre perl tzdata libcap su-exec zip 	&& wget -O kong.tar.gz "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.amd64.apk.tar.gz" 	&& echo "$KONG_SHA256 *kong.tar.gz" | sha256sum -c - 	&& tar -xzf kong.tar.gz -C /tmp 	&& rm -f kong.tar.gz 	&& cp -R /tmp/usr / 	&& rm -rf /tmp/usr 	&& cp -R /tmp/etc / 	&& rm -rf /tmp/etc 	&& apk del .build-deps 	&& chown -R kong:0 /usr/local/kong 	&& chmod -R g=u /usr/local/kong
# Tue, 14 Jan 2020 22:20:10 GMT
COPY file:fe196e90eb453e834bdc492372019ad9f95e35142fa279d1622c213f32592fe9 in /docker-entrypoint.sh 
# Tue, 14 Jan 2020 22:20:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2020 22:20:11 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 14 Jan 2020 22:20:11 GMT
STOPSIGNAL SIGQUIT
# Tue, 14 Jan 2020 22:20:11 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:89d9c30c1d48bac627e5c6cb0d1ed1eec28e7dbdfbcc04712e4c79c0f83faf17`  
		Last Modified: Mon, 21 Oct 2019 17:22:48 GMT  
		Size: 2.8 MB (2787134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efff247f0f0be1c48baef7a6084e579e819895ac650e8658328d72277d930da8`  
		Last Modified: Tue, 14 Jan 2020 22:24:14 GMT  
		Size: 41.3 MB (41328424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc63fcd4751cea13596e7526721665e012cb861f64db41cc5659c016403207c`  
		Last Modified: Tue, 14 Jan 2020 22:24:06 GMT  
		Size: 597.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
