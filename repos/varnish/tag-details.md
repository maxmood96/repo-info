<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `varnish`

-	[`varnish:6`](#varnish6)
-	[`varnish:6.0`](#varnish60)
-	[`varnish:6.0.6`](#varnish606)
-	[`varnish:6.0.6-1`](#varnish606-1)
-	[`varnish:6.4`](#varnish64)
-	[`varnish:6.4.0`](#varnish640)
-	[`varnish:6.4.0-1`](#varnish640-1)
-	[`varnish:fresh`](#varnishfresh)
-	[`varnish:latest`](#varnishlatest)
-	[`varnish:stable`](#varnishstable)

## `varnish:6`

```console
$ docker pull varnish@sha256:d125291aa85fedb7e2f84ec60cd377f11e64439b06c4fd643e69f49b09297b9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:6` - linux; amd64

```console
$ docker pull varnish@sha256:888d7b1d49d1b1d920ffc5dada194b9762dfda925cebf588a0343918651b78d1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76774250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c676e0026b42aff03367c9f376fe7422800f0225ed024793bb62257cbafb5c34`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 16 Apr 2020 03:22:36 GMT
ADD file:865f9041e12eb341f0a394764ddc11db49cbc8b91d4fb57c6fb1960b68b1bb41 in / 
# Thu, 16 Apr 2020 03:22:36 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 03:52:47 GMT
ENV VARNISH_VERSION=6.4.0-1~buster
# Thu, 16 Apr 2020 03:52:47 GMT
ENV VARNISH_SIZE=100M
# Thu, 16 Apr 2020 03:53:21 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=A9897320C397E3A60C03E8BF821AD320F71BFF3D; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://hkps.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish64/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 03:53:22 GMT
WORKDIR /etc/varnish
# Thu, 16 Apr 2020 03:53:22 GMT
COPY file:4156d91450dca54febf2b6908a0871cf84271dba1069d9641be798ec9f560393 in /usr/local/bin/ 
# Thu, 16 Apr 2020 03:53:22 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Thu, 16 Apr 2020 03:53:22 GMT
EXPOSE 80 8443
# Thu, 16 Apr 2020 03:53:22 GMT
CMD []
```

-	Layers:
	-	`sha256:123275d6e508d282237a22fefa5aef822b719a06496444ea89efa65da523fc4b`  
		Last Modified: Thu, 16 Apr 2020 03:31:44 GMT  
		Size: 27.1 MB (27098147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb311f31e0f2f1520c2a23e150d65519bfb5346870c90041e239e3008969148c`  
		Last Modified: Thu, 16 Apr 2020 03:54:01 GMT  
		Size: 49.7 MB (49675652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60c47e9ab4526d95b7f5193aae2c310adc2f41f1f3521ad62f92a06f6de41979`  
		Last Modified: Thu, 16 Apr 2020 03:53:49 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.0`

```console
$ docker pull varnish@sha256:18c64e27fda812e885bb9f253b5295e13bb7606a531789c506c09a731aa44af1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:6.0` - linux; amd64

```console
$ docker pull varnish@sha256:11fff492aea7e6e118d305387dde3ea38401627be30fec832e2b13ec7f127a1b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67208636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d53eabdaf385ac44e7c5528ea3ec54136ecdbeee155eea23bf4bd4626b2b9d2`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 16 Apr 2020 03:27:50 GMT
ADD file:40f52c233aecabf572a9db7450590d54d5e125fb00ecbb4a26fecd0b71e84eb8 in / 
# Thu, 16 Apr 2020 03:27:50 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 03:51:37 GMT
ENV VARNISH_VERSION=6.0.6-1~stretch
# Thu, 16 Apr 2020 03:51:38 GMT
ENV VARNISH_SIZE=100M
# Thu, 16 Apr 2020 03:52:39 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=48D81A24CB0456F5D59431D94CFCFD6BA750EDCD; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://hkps.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish60lts/debian/ stretch main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 03:52:39 GMT
WORKDIR /etc/varnish
# Thu, 16 Apr 2020 03:52:40 GMT
COPY file:4156d91450dca54febf2b6908a0871cf84271dba1069d9641be798ec9f560393 in /usr/local/bin/ 
# Thu, 16 Apr 2020 03:52:40 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Thu, 16 Apr 2020 03:52:41 GMT
EXPOSE 80 8443
# Thu, 16 Apr 2020 03:52:41 GMT
CMD []
```

-	Layers:
	-	`sha256:5e35bd43cf7898d036f8515be74d45b2e3abd2a5534fc280de63a9c22dd175bd`  
		Last Modified: Thu, 16 Apr 2020 03:35:04 GMT  
		Size: 22.5 MB (22513476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c17b6afc732b85d089ed8ef9b18f81774d27afdf4f7317da1f5bbca067329631`  
		Last Modified: Thu, 16 Apr 2020 03:53:43 GMT  
		Size: 44.7 MB (44694700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c93847cfca59844b1178a71325c5d7aacb58543757555f67a296c59caad896`  
		Last Modified: Thu, 16 Apr 2020 03:53:33 GMT  
		Size: 460.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.0.6`

```console
$ docker pull varnish@sha256:18c64e27fda812e885bb9f253b5295e13bb7606a531789c506c09a731aa44af1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:6.0.6` - linux; amd64

```console
$ docker pull varnish@sha256:11fff492aea7e6e118d305387dde3ea38401627be30fec832e2b13ec7f127a1b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67208636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d53eabdaf385ac44e7c5528ea3ec54136ecdbeee155eea23bf4bd4626b2b9d2`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 16 Apr 2020 03:27:50 GMT
ADD file:40f52c233aecabf572a9db7450590d54d5e125fb00ecbb4a26fecd0b71e84eb8 in / 
# Thu, 16 Apr 2020 03:27:50 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 03:51:37 GMT
ENV VARNISH_VERSION=6.0.6-1~stretch
# Thu, 16 Apr 2020 03:51:38 GMT
ENV VARNISH_SIZE=100M
# Thu, 16 Apr 2020 03:52:39 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=48D81A24CB0456F5D59431D94CFCFD6BA750EDCD; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://hkps.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish60lts/debian/ stretch main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 03:52:39 GMT
WORKDIR /etc/varnish
# Thu, 16 Apr 2020 03:52:40 GMT
COPY file:4156d91450dca54febf2b6908a0871cf84271dba1069d9641be798ec9f560393 in /usr/local/bin/ 
# Thu, 16 Apr 2020 03:52:40 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Thu, 16 Apr 2020 03:52:41 GMT
EXPOSE 80 8443
# Thu, 16 Apr 2020 03:52:41 GMT
CMD []
```

-	Layers:
	-	`sha256:5e35bd43cf7898d036f8515be74d45b2e3abd2a5534fc280de63a9c22dd175bd`  
		Last Modified: Thu, 16 Apr 2020 03:35:04 GMT  
		Size: 22.5 MB (22513476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c17b6afc732b85d089ed8ef9b18f81774d27afdf4f7317da1f5bbca067329631`  
		Last Modified: Thu, 16 Apr 2020 03:53:43 GMT  
		Size: 44.7 MB (44694700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c93847cfca59844b1178a71325c5d7aacb58543757555f67a296c59caad896`  
		Last Modified: Thu, 16 Apr 2020 03:53:33 GMT  
		Size: 460.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.0.6-1`

```console
$ docker pull varnish@sha256:18c64e27fda812e885bb9f253b5295e13bb7606a531789c506c09a731aa44af1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:6.0.6-1` - linux; amd64

```console
$ docker pull varnish@sha256:11fff492aea7e6e118d305387dde3ea38401627be30fec832e2b13ec7f127a1b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67208636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d53eabdaf385ac44e7c5528ea3ec54136ecdbeee155eea23bf4bd4626b2b9d2`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 16 Apr 2020 03:27:50 GMT
ADD file:40f52c233aecabf572a9db7450590d54d5e125fb00ecbb4a26fecd0b71e84eb8 in / 
# Thu, 16 Apr 2020 03:27:50 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 03:51:37 GMT
ENV VARNISH_VERSION=6.0.6-1~stretch
# Thu, 16 Apr 2020 03:51:38 GMT
ENV VARNISH_SIZE=100M
# Thu, 16 Apr 2020 03:52:39 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=48D81A24CB0456F5D59431D94CFCFD6BA750EDCD; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://hkps.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish60lts/debian/ stretch main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 03:52:39 GMT
WORKDIR /etc/varnish
# Thu, 16 Apr 2020 03:52:40 GMT
COPY file:4156d91450dca54febf2b6908a0871cf84271dba1069d9641be798ec9f560393 in /usr/local/bin/ 
# Thu, 16 Apr 2020 03:52:40 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Thu, 16 Apr 2020 03:52:41 GMT
EXPOSE 80 8443
# Thu, 16 Apr 2020 03:52:41 GMT
CMD []
```

-	Layers:
	-	`sha256:5e35bd43cf7898d036f8515be74d45b2e3abd2a5534fc280de63a9c22dd175bd`  
		Last Modified: Thu, 16 Apr 2020 03:35:04 GMT  
		Size: 22.5 MB (22513476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c17b6afc732b85d089ed8ef9b18f81774d27afdf4f7317da1f5bbca067329631`  
		Last Modified: Thu, 16 Apr 2020 03:53:43 GMT  
		Size: 44.7 MB (44694700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c93847cfca59844b1178a71325c5d7aacb58543757555f67a296c59caad896`  
		Last Modified: Thu, 16 Apr 2020 03:53:33 GMT  
		Size: 460.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.4`

```console
$ docker pull varnish@sha256:d125291aa85fedb7e2f84ec60cd377f11e64439b06c4fd643e69f49b09297b9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:6.4` - linux; amd64

```console
$ docker pull varnish@sha256:888d7b1d49d1b1d920ffc5dada194b9762dfda925cebf588a0343918651b78d1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76774250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c676e0026b42aff03367c9f376fe7422800f0225ed024793bb62257cbafb5c34`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 16 Apr 2020 03:22:36 GMT
ADD file:865f9041e12eb341f0a394764ddc11db49cbc8b91d4fb57c6fb1960b68b1bb41 in / 
# Thu, 16 Apr 2020 03:22:36 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 03:52:47 GMT
ENV VARNISH_VERSION=6.4.0-1~buster
# Thu, 16 Apr 2020 03:52:47 GMT
ENV VARNISH_SIZE=100M
# Thu, 16 Apr 2020 03:53:21 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=A9897320C397E3A60C03E8BF821AD320F71BFF3D; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://hkps.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish64/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 03:53:22 GMT
WORKDIR /etc/varnish
# Thu, 16 Apr 2020 03:53:22 GMT
COPY file:4156d91450dca54febf2b6908a0871cf84271dba1069d9641be798ec9f560393 in /usr/local/bin/ 
# Thu, 16 Apr 2020 03:53:22 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Thu, 16 Apr 2020 03:53:22 GMT
EXPOSE 80 8443
# Thu, 16 Apr 2020 03:53:22 GMT
CMD []
```

-	Layers:
	-	`sha256:123275d6e508d282237a22fefa5aef822b719a06496444ea89efa65da523fc4b`  
		Last Modified: Thu, 16 Apr 2020 03:31:44 GMT  
		Size: 27.1 MB (27098147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb311f31e0f2f1520c2a23e150d65519bfb5346870c90041e239e3008969148c`  
		Last Modified: Thu, 16 Apr 2020 03:54:01 GMT  
		Size: 49.7 MB (49675652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60c47e9ab4526d95b7f5193aae2c310adc2f41f1f3521ad62f92a06f6de41979`  
		Last Modified: Thu, 16 Apr 2020 03:53:49 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.4.0`

```console
$ docker pull varnish@sha256:d125291aa85fedb7e2f84ec60cd377f11e64439b06c4fd643e69f49b09297b9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:6.4.0` - linux; amd64

```console
$ docker pull varnish@sha256:888d7b1d49d1b1d920ffc5dada194b9762dfda925cebf588a0343918651b78d1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76774250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c676e0026b42aff03367c9f376fe7422800f0225ed024793bb62257cbafb5c34`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 16 Apr 2020 03:22:36 GMT
ADD file:865f9041e12eb341f0a394764ddc11db49cbc8b91d4fb57c6fb1960b68b1bb41 in / 
# Thu, 16 Apr 2020 03:22:36 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 03:52:47 GMT
ENV VARNISH_VERSION=6.4.0-1~buster
# Thu, 16 Apr 2020 03:52:47 GMT
ENV VARNISH_SIZE=100M
# Thu, 16 Apr 2020 03:53:21 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=A9897320C397E3A60C03E8BF821AD320F71BFF3D; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://hkps.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish64/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 03:53:22 GMT
WORKDIR /etc/varnish
# Thu, 16 Apr 2020 03:53:22 GMT
COPY file:4156d91450dca54febf2b6908a0871cf84271dba1069d9641be798ec9f560393 in /usr/local/bin/ 
# Thu, 16 Apr 2020 03:53:22 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Thu, 16 Apr 2020 03:53:22 GMT
EXPOSE 80 8443
# Thu, 16 Apr 2020 03:53:22 GMT
CMD []
```

-	Layers:
	-	`sha256:123275d6e508d282237a22fefa5aef822b719a06496444ea89efa65da523fc4b`  
		Last Modified: Thu, 16 Apr 2020 03:31:44 GMT  
		Size: 27.1 MB (27098147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb311f31e0f2f1520c2a23e150d65519bfb5346870c90041e239e3008969148c`  
		Last Modified: Thu, 16 Apr 2020 03:54:01 GMT  
		Size: 49.7 MB (49675652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60c47e9ab4526d95b7f5193aae2c310adc2f41f1f3521ad62f92a06f6de41979`  
		Last Modified: Thu, 16 Apr 2020 03:53:49 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.4.0-1`

```console
$ docker pull varnish@sha256:d125291aa85fedb7e2f84ec60cd377f11e64439b06c4fd643e69f49b09297b9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:6.4.0-1` - linux; amd64

```console
$ docker pull varnish@sha256:888d7b1d49d1b1d920ffc5dada194b9762dfda925cebf588a0343918651b78d1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76774250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c676e0026b42aff03367c9f376fe7422800f0225ed024793bb62257cbafb5c34`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 16 Apr 2020 03:22:36 GMT
ADD file:865f9041e12eb341f0a394764ddc11db49cbc8b91d4fb57c6fb1960b68b1bb41 in / 
# Thu, 16 Apr 2020 03:22:36 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 03:52:47 GMT
ENV VARNISH_VERSION=6.4.0-1~buster
# Thu, 16 Apr 2020 03:52:47 GMT
ENV VARNISH_SIZE=100M
# Thu, 16 Apr 2020 03:53:21 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=A9897320C397E3A60C03E8BF821AD320F71BFF3D; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://hkps.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish64/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 03:53:22 GMT
WORKDIR /etc/varnish
# Thu, 16 Apr 2020 03:53:22 GMT
COPY file:4156d91450dca54febf2b6908a0871cf84271dba1069d9641be798ec9f560393 in /usr/local/bin/ 
# Thu, 16 Apr 2020 03:53:22 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Thu, 16 Apr 2020 03:53:22 GMT
EXPOSE 80 8443
# Thu, 16 Apr 2020 03:53:22 GMT
CMD []
```

-	Layers:
	-	`sha256:123275d6e508d282237a22fefa5aef822b719a06496444ea89efa65da523fc4b`  
		Last Modified: Thu, 16 Apr 2020 03:31:44 GMT  
		Size: 27.1 MB (27098147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb311f31e0f2f1520c2a23e150d65519bfb5346870c90041e239e3008969148c`  
		Last Modified: Thu, 16 Apr 2020 03:54:01 GMT  
		Size: 49.7 MB (49675652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60c47e9ab4526d95b7f5193aae2c310adc2f41f1f3521ad62f92a06f6de41979`  
		Last Modified: Thu, 16 Apr 2020 03:53:49 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:fresh`

```console
$ docker pull varnish@sha256:d125291aa85fedb7e2f84ec60cd377f11e64439b06c4fd643e69f49b09297b9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:fresh` - linux; amd64

```console
$ docker pull varnish@sha256:888d7b1d49d1b1d920ffc5dada194b9762dfda925cebf588a0343918651b78d1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76774250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c676e0026b42aff03367c9f376fe7422800f0225ed024793bb62257cbafb5c34`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 16 Apr 2020 03:22:36 GMT
ADD file:865f9041e12eb341f0a394764ddc11db49cbc8b91d4fb57c6fb1960b68b1bb41 in / 
# Thu, 16 Apr 2020 03:22:36 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 03:52:47 GMT
ENV VARNISH_VERSION=6.4.0-1~buster
# Thu, 16 Apr 2020 03:52:47 GMT
ENV VARNISH_SIZE=100M
# Thu, 16 Apr 2020 03:53:21 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=A9897320C397E3A60C03E8BF821AD320F71BFF3D; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://hkps.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish64/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 03:53:22 GMT
WORKDIR /etc/varnish
# Thu, 16 Apr 2020 03:53:22 GMT
COPY file:4156d91450dca54febf2b6908a0871cf84271dba1069d9641be798ec9f560393 in /usr/local/bin/ 
# Thu, 16 Apr 2020 03:53:22 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Thu, 16 Apr 2020 03:53:22 GMT
EXPOSE 80 8443
# Thu, 16 Apr 2020 03:53:22 GMT
CMD []
```

-	Layers:
	-	`sha256:123275d6e508d282237a22fefa5aef822b719a06496444ea89efa65da523fc4b`  
		Last Modified: Thu, 16 Apr 2020 03:31:44 GMT  
		Size: 27.1 MB (27098147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb311f31e0f2f1520c2a23e150d65519bfb5346870c90041e239e3008969148c`  
		Last Modified: Thu, 16 Apr 2020 03:54:01 GMT  
		Size: 49.7 MB (49675652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60c47e9ab4526d95b7f5193aae2c310adc2f41f1f3521ad62f92a06f6de41979`  
		Last Modified: Thu, 16 Apr 2020 03:53:49 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:latest`

```console
$ docker pull varnish@sha256:d125291aa85fedb7e2f84ec60cd377f11e64439b06c4fd643e69f49b09297b9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:latest` - linux; amd64

```console
$ docker pull varnish@sha256:888d7b1d49d1b1d920ffc5dada194b9762dfda925cebf588a0343918651b78d1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76774250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c676e0026b42aff03367c9f376fe7422800f0225ed024793bb62257cbafb5c34`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 16 Apr 2020 03:22:36 GMT
ADD file:865f9041e12eb341f0a394764ddc11db49cbc8b91d4fb57c6fb1960b68b1bb41 in / 
# Thu, 16 Apr 2020 03:22:36 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 03:52:47 GMT
ENV VARNISH_VERSION=6.4.0-1~buster
# Thu, 16 Apr 2020 03:52:47 GMT
ENV VARNISH_SIZE=100M
# Thu, 16 Apr 2020 03:53:21 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=A9897320C397E3A60C03E8BF821AD320F71BFF3D; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://hkps.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish64/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 03:53:22 GMT
WORKDIR /etc/varnish
# Thu, 16 Apr 2020 03:53:22 GMT
COPY file:4156d91450dca54febf2b6908a0871cf84271dba1069d9641be798ec9f560393 in /usr/local/bin/ 
# Thu, 16 Apr 2020 03:53:22 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Thu, 16 Apr 2020 03:53:22 GMT
EXPOSE 80 8443
# Thu, 16 Apr 2020 03:53:22 GMT
CMD []
```

-	Layers:
	-	`sha256:123275d6e508d282237a22fefa5aef822b719a06496444ea89efa65da523fc4b`  
		Last Modified: Thu, 16 Apr 2020 03:31:44 GMT  
		Size: 27.1 MB (27098147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb311f31e0f2f1520c2a23e150d65519bfb5346870c90041e239e3008969148c`  
		Last Modified: Thu, 16 Apr 2020 03:54:01 GMT  
		Size: 49.7 MB (49675652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60c47e9ab4526d95b7f5193aae2c310adc2f41f1f3521ad62f92a06f6de41979`  
		Last Modified: Thu, 16 Apr 2020 03:53:49 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:stable`

```console
$ docker pull varnish@sha256:18c64e27fda812e885bb9f253b5295e13bb7606a531789c506c09a731aa44af1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:stable` - linux; amd64

```console
$ docker pull varnish@sha256:11fff492aea7e6e118d305387dde3ea38401627be30fec832e2b13ec7f127a1b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67208636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d53eabdaf385ac44e7c5528ea3ec54136ecdbeee155eea23bf4bd4626b2b9d2`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 16 Apr 2020 03:27:50 GMT
ADD file:40f52c233aecabf572a9db7450590d54d5e125fb00ecbb4a26fecd0b71e84eb8 in / 
# Thu, 16 Apr 2020 03:27:50 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 03:51:37 GMT
ENV VARNISH_VERSION=6.0.6-1~stretch
# Thu, 16 Apr 2020 03:51:38 GMT
ENV VARNISH_SIZE=100M
# Thu, 16 Apr 2020 03:52:39 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=48D81A24CB0456F5D59431D94CFCFD6BA750EDCD; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://hkps.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish60lts/debian/ stretch main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 03:52:39 GMT
WORKDIR /etc/varnish
# Thu, 16 Apr 2020 03:52:40 GMT
COPY file:4156d91450dca54febf2b6908a0871cf84271dba1069d9641be798ec9f560393 in /usr/local/bin/ 
# Thu, 16 Apr 2020 03:52:40 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Thu, 16 Apr 2020 03:52:41 GMT
EXPOSE 80 8443
# Thu, 16 Apr 2020 03:52:41 GMT
CMD []
```

-	Layers:
	-	`sha256:5e35bd43cf7898d036f8515be74d45b2e3abd2a5534fc280de63a9c22dd175bd`  
		Last Modified: Thu, 16 Apr 2020 03:35:04 GMT  
		Size: 22.5 MB (22513476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c17b6afc732b85d089ed8ef9b18f81774d27afdf4f7317da1f5bbca067329631`  
		Last Modified: Thu, 16 Apr 2020 03:53:43 GMT  
		Size: 44.7 MB (44694700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c93847cfca59844b1178a71325c5d7aacb58543757555f67a296c59caad896`  
		Last Modified: Thu, 16 Apr 2020 03:53:33 GMT  
		Size: 460.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
