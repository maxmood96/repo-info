## `varnish:stable`

```console
$ docker pull varnish@sha256:2b51cb720a3277ff15d10ec67e7bf8a417fdb782df731c0e5e92a6e97536b7aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:stable` - linux; amd64

```console
$ docker pull varnish@sha256:5054430b542db7e207a124fd491a6b468585b8b9ce2c8385aa60175aa3987800
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67182409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a03ec5845def7cd0960039723994384c4811a118d66e0bbbf5eb1c790ebe4f64`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 09 Jun 2020 01:23:35 GMT
ADD file:57b431451a292755d0f13673f5f3bea9f62aea36c7a1b59d34d7d200ba134fea in / 
# Tue, 09 Jun 2020 01:23:35 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 02:18:05 GMT
ENV VARNISH_VERSION=6.0.6-1~stretch
# Tue, 09 Jun 2020 02:18:05 GMT
ENV VARNISH_SIZE=100M
# Tue, 09 Jun 2020 02:18:32 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=48D81A24CB0456F5D59431D94CFCFD6BA750EDCD; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://hkps.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish60lts/debian/ stretch main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 02:18:32 GMT
WORKDIR /etc/varnish
# Tue, 09 Jun 2020 02:18:33 GMT
COPY file:4156d91450dca54febf2b6908a0871cf84271dba1069d9641be798ec9f560393 in /usr/local/bin/ 
# Tue, 09 Jun 2020 02:18:33 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Tue, 09 Jun 2020 02:18:34 GMT
EXPOSE 80 8443
# Tue, 09 Jun 2020 02:18:34 GMT
CMD []
```

-	Layers:
	-	`sha256:7d2977b12acb33f192e3f20b7e15a467cc8f3f5124a15d975a6d4afe5fa3d258`  
		Last Modified: Tue, 09 Jun 2020 01:28:13 GMT  
		Size: 22.5 MB (22519600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:552c7e657c95e7eab3d8aa333845f45f85effe0475ccbe07f2c15f7465fb462e`  
		Last Modified: Tue, 09 Jun 2020 02:19:26 GMT  
		Size: 44.7 MB (44662349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74a2007aacf31c12801a387400f28190aaf6eed5ab5b7a5816653fc06e602479`  
		Last Modified: Tue, 09 Jun 2020 02:19:19 GMT  
		Size: 460.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
