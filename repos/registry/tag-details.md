<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `registry`

-	[`registry:2`](#registry2)
-	[`registry:2.7`](#registry27)
-	[`registry:2.7.1`](#registry271)
-	[`registry:latest`](#registrylatest)

## `registry:2`

```console
$ docker pull registry@sha256:9bd4d195c5daf7abf4703e36e0c1423181ad6de9f06d737c61bb33610fb8b585
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `registry:2` - linux; amd64

```console
$ docker pull registry@sha256:e09ed8c6c837d366a501f15dcb47939bbbb6242bf3886270834e2a0fa1555234
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9937424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d4f4b5309b1e41b4f83ae59b44df6d673ef44433c734b14c1c103ebca82c116`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Thu, 18 Jun 2020 18:20:04 GMT
RUN set -ex     && apk add --no-cache ca-certificates
# Thu, 18 Jun 2020 18:20:04 GMT
COPY file:21256ff7df5369f7ad2e19c6d020a644303aded200bdbec4d46648f38d55df78 in /bin/registry 
# Thu, 18 Jun 2020 18:20:04 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 18 Jun 2020 18:20:04 GMT
VOLUME [/var/lib/registry]
# Thu, 18 Jun 2020 18:20:05 GMT
EXPOSE 5000
# Thu, 18 Jun 2020 18:20:05 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 18 Jun 2020 18:20:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Jun 2020 18:20:05 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47112e65547dd36dc84ab7aac240f297c424b449d78335758620967bed8ea845`  
		Last Modified: Thu, 18 Jun 2020 18:20:13 GMT  
		Size: 299.6 KB (299598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46bcb632e50679325611e71844537bebdb70fc1bf9021e052d783088477322c4`  
		Last Modified: Thu, 18 Jun 2020 18:20:14 GMT  
		Size: 6.8 MB (6823927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1cc712bcecda5c187b281d8452745a2593f4dedda30a4bc32b49263e81e5bc6`  
		Last Modified: Thu, 18 Jun 2020 18:20:12 GMT  
		Size: 370.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3db6272dcbfa9e8cb78cf93f1119d2c4960b628623d7c077ddd97047613468ff`  
		Last Modified: Thu, 18 Jun 2020 18:20:13 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2` - linux; arm variant v6

```console
$ docker pull registry@sha256:c8c97b4d572c33156da59bae82f6b833abf5ceaa69bb18d002406c2891fce4a8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9312382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2126abe3746bfb8bd3bccc38ecc00d331a3bad9db38232c473ddf04e92c2078a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 16 Dec 2020 23:49:53 GMT
ADD file:e3a6f7566ee3c2ba61d27d801d3522e045a4be64a42f32ee52d933b68338d06f in / 
# Wed, 16 Dec 2020 23:49:55 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 07:52:08 GMT
RUN set -ex     && apk add --no-cache ca-certificates
# Thu, 17 Dec 2020 07:52:09 GMT
COPY file:29c6c1625420a558a03cc7ed253192f8138cba6212b64e30217fb6488af668e2 in /bin/registry 
# Thu, 17 Dec 2020 07:52:10 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 17 Dec 2020 07:52:12 GMT
VOLUME [/var/lib/registry]
# Thu, 17 Dec 2020 07:52:13 GMT
EXPOSE 5000
# Thu, 17 Dec 2020 07:52:14 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 17 Dec 2020 07:52:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Dec 2020 07:52:16 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:56fec67ad66eea034cf5b7d0d0ffd355c0fe87611bad132ac5a952fcaa52138b`  
		Last Modified: Wed, 16 Dec 2020 23:50:34 GMT  
		Size: 2.6 MB (2620769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf7cc14966ceb5e5b46be135c16f21f7af42f270518ed92962f9514d0874ce7d`  
		Last Modified: Thu, 17 Dec 2020 07:52:29 GMT  
		Size: 299.9 KB (299919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96618f9c1a201fedc2049c85c36fc0b4a817442c4f712140f49d76310034d2f7`  
		Last Modified: Thu, 17 Dec 2020 07:52:33 GMT  
		Size: 6.4 MB (6391083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5acb2c1463288a9621bede426350b5e343e6beb7639ab71ea9be3cd67599bb52`  
		Last Modified: Thu, 17 Dec 2020 07:52:28 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9b1ea70368acb9d8c55ea555a87c799805882309d54ad7af9aa7d8e1d8b366`  
		Last Modified: Thu, 17 Dec 2020 07:52:29 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:df3e5e623e469600373cb327e8788e4eeb5e4a4c48e58461feb2b0d4c7f3c588
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9265349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1525b096095b7c89c39f47897379a700ca4a56864a18fd60c35dbb46cbf4cb9a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Thu, 18 Jun 2020 17:40:29 GMT
RUN set -ex     && apk add --no-cache ca-certificates
# Thu, 18 Jun 2020 17:40:29 GMT
COPY file:51a441e6eceff49ef32609e7070b64e8d5690648e4f915cc825274e6fe37aed2 in /bin/registry 
# Thu, 18 Jun 2020 17:40:30 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 18 Jun 2020 17:40:31 GMT
VOLUME [/var/lib/registry]
# Thu, 18 Jun 2020 17:40:31 GMT
EXPOSE 5000
# Thu, 18 Jun 2020 17:40:32 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 18 Jun 2020 17:40:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Jun 2020 17:40:33 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e44ffe5a70335b9c005f5ce0f0fcbbebb301d9b6440409c5b868dabcd86c9ba`  
		Last Modified: Thu, 18 Jun 2020 17:40:43 GMT  
		Size: 300.1 KB (300114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc788ee7896b71758970563ffa9bd4deb180dee6000984911138c49e9eba6a23`  
		Last Modified: Thu, 18 Jun 2020 17:40:45 GMT  
		Size: 6.2 MB (6240198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f89902f2529afb002c788b9e561f9798a8fe5ed45ab604447bb88e77528761bb`  
		Last Modified: Thu, 18 Jun 2020 17:40:44 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:215110f71eb42468d3edb51073d4e8e18bbdbd09c491a9b72240efeb4f6ec263`  
		Last Modified: Thu, 18 Jun 2020 17:40:44 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `registry:2.7`

```console
$ docker pull registry@sha256:9bd4d195c5daf7abf4703e36e0c1423181ad6de9f06d737c61bb33610fb8b585
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `registry:2.7` - linux; amd64

```console
$ docker pull registry@sha256:e09ed8c6c837d366a501f15dcb47939bbbb6242bf3886270834e2a0fa1555234
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9937424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d4f4b5309b1e41b4f83ae59b44df6d673ef44433c734b14c1c103ebca82c116`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Thu, 18 Jun 2020 18:20:04 GMT
RUN set -ex     && apk add --no-cache ca-certificates
# Thu, 18 Jun 2020 18:20:04 GMT
COPY file:21256ff7df5369f7ad2e19c6d020a644303aded200bdbec4d46648f38d55df78 in /bin/registry 
# Thu, 18 Jun 2020 18:20:04 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 18 Jun 2020 18:20:04 GMT
VOLUME [/var/lib/registry]
# Thu, 18 Jun 2020 18:20:05 GMT
EXPOSE 5000
# Thu, 18 Jun 2020 18:20:05 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 18 Jun 2020 18:20:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Jun 2020 18:20:05 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47112e65547dd36dc84ab7aac240f297c424b449d78335758620967bed8ea845`  
		Last Modified: Thu, 18 Jun 2020 18:20:13 GMT  
		Size: 299.6 KB (299598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46bcb632e50679325611e71844537bebdb70fc1bf9021e052d783088477322c4`  
		Last Modified: Thu, 18 Jun 2020 18:20:14 GMT  
		Size: 6.8 MB (6823927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1cc712bcecda5c187b281d8452745a2593f4dedda30a4bc32b49263e81e5bc6`  
		Last Modified: Thu, 18 Jun 2020 18:20:12 GMT  
		Size: 370.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3db6272dcbfa9e8cb78cf93f1119d2c4960b628623d7c077ddd97047613468ff`  
		Last Modified: Thu, 18 Jun 2020 18:20:13 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.7` - linux; arm variant v6

```console
$ docker pull registry@sha256:c8c97b4d572c33156da59bae82f6b833abf5ceaa69bb18d002406c2891fce4a8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9312382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2126abe3746bfb8bd3bccc38ecc00d331a3bad9db38232c473ddf04e92c2078a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 16 Dec 2020 23:49:53 GMT
ADD file:e3a6f7566ee3c2ba61d27d801d3522e045a4be64a42f32ee52d933b68338d06f in / 
# Wed, 16 Dec 2020 23:49:55 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 07:52:08 GMT
RUN set -ex     && apk add --no-cache ca-certificates
# Thu, 17 Dec 2020 07:52:09 GMT
COPY file:29c6c1625420a558a03cc7ed253192f8138cba6212b64e30217fb6488af668e2 in /bin/registry 
# Thu, 17 Dec 2020 07:52:10 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 17 Dec 2020 07:52:12 GMT
VOLUME [/var/lib/registry]
# Thu, 17 Dec 2020 07:52:13 GMT
EXPOSE 5000
# Thu, 17 Dec 2020 07:52:14 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 17 Dec 2020 07:52:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Dec 2020 07:52:16 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:56fec67ad66eea034cf5b7d0d0ffd355c0fe87611bad132ac5a952fcaa52138b`  
		Last Modified: Wed, 16 Dec 2020 23:50:34 GMT  
		Size: 2.6 MB (2620769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf7cc14966ceb5e5b46be135c16f21f7af42f270518ed92962f9514d0874ce7d`  
		Last Modified: Thu, 17 Dec 2020 07:52:29 GMT  
		Size: 299.9 KB (299919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96618f9c1a201fedc2049c85c36fc0b4a817442c4f712140f49d76310034d2f7`  
		Last Modified: Thu, 17 Dec 2020 07:52:33 GMT  
		Size: 6.4 MB (6391083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5acb2c1463288a9621bede426350b5e343e6beb7639ab71ea9be3cd67599bb52`  
		Last Modified: Thu, 17 Dec 2020 07:52:28 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9b1ea70368acb9d8c55ea555a87c799805882309d54ad7af9aa7d8e1d8b366`  
		Last Modified: Thu, 17 Dec 2020 07:52:29 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.7` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:df3e5e623e469600373cb327e8788e4eeb5e4a4c48e58461feb2b0d4c7f3c588
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9265349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1525b096095b7c89c39f47897379a700ca4a56864a18fd60c35dbb46cbf4cb9a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Thu, 18 Jun 2020 17:40:29 GMT
RUN set -ex     && apk add --no-cache ca-certificates
# Thu, 18 Jun 2020 17:40:29 GMT
COPY file:51a441e6eceff49ef32609e7070b64e8d5690648e4f915cc825274e6fe37aed2 in /bin/registry 
# Thu, 18 Jun 2020 17:40:30 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 18 Jun 2020 17:40:31 GMT
VOLUME [/var/lib/registry]
# Thu, 18 Jun 2020 17:40:31 GMT
EXPOSE 5000
# Thu, 18 Jun 2020 17:40:32 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 18 Jun 2020 17:40:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Jun 2020 17:40:33 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e44ffe5a70335b9c005f5ce0f0fcbbebb301d9b6440409c5b868dabcd86c9ba`  
		Last Modified: Thu, 18 Jun 2020 17:40:43 GMT  
		Size: 300.1 KB (300114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc788ee7896b71758970563ffa9bd4deb180dee6000984911138c49e9eba6a23`  
		Last Modified: Thu, 18 Jun 2020 17:40:45 GMT  
		Size: 6.2 MB (6240198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f89902f2529afb002c788b9e561f9798a8fe5ed45ab604447bb88e77528761bb`  
		Last Modified: Thu, 18 Jun 2020 17:40:44 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:215110f71eb42468d3edb51073d4e8e18bbdbd09c491a9b72240efeb4f6ec263`  
		Last Modified: Thu, 18 Jun 2020 17:40:44 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `registry:2.7.1`

```console
$ docker pull registry@sha256:9bd4d195c5daf7abf4703e36e0c1423181ad6de9f06d737c61bb33610fb8b585
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `registry:2.7.1` - linux; amd64

```console
$ docker pull registry@sha256:e09ed8c6c837d366a501f15dcb47939bbbb6242bf3886270834e2a0fa1555234
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9937424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d4f4b5309b1e41b4f83ae59b44df6d673ef44433c734b14c1c103ebca82c116`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Thu, 18 Jun 2020 18:20:04 GMT
RUN set -ex     && apk add --no-cache ca-certificates
# Thu, 18 Jun 2020 18:20:04 GMT
COPY file:21256ff7df5369f7ad2e19c6d020a644303aded200bdbec4d46648f38d55df78 in /bin/registry 
# Thu, 18 Jun 2020 18:20:04 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 18 Jun 2020 18:20:04 GMT
VOLUME [/var/lib/registry]
# Thu, 18 Jun 2020 18:20:05 GMT
EXPOSE 5000
# Thu, 18 Jun 2020 18:20:05 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 18 Jun 2020 18:20:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Jun 2020 18:20:05 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47112e65547dd36dc84ab7aac240f297c424b449d78335758620967bed8ea845`  
		Last Modified: Thu, 18 Jun 2020 18:20:13 GMT  
		Size: 299.6 KB (299598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46bcb632e50679325611e71844537bebdb70fc1bf9021e052d783088477322c4`  
		Last Modified: Thu, 18 Jun 2020 18:20:14 GMT  
		Size: 6.8 MB (6823927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1cc712bcecda5c187b281d8452745a2593f4dedda30a4bc32b49263e81e5bc6`  
		Last Modified: Thu, 18 Jun 2020 18:20:12 GMT  
		Size: 370.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3db6272dcbfa9e8cb78cf93f1119d2c4960b628623d7c077ddd97047613468ff`  
		Last Modified: Thu, 18 Jun 2020 18:20:13 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.7.1` - linux; arm variant v6

```console
$ docker pull registry@sha256:c8c97b4d572c33156da59bae82f6b833abf5ceaa69bb18d002406c2891fce4a8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9312382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2126abe3746bfb8bd3bccc38ecc00d331a3bad9db38232c473ddf04e92c2078a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 16 Dec 2020 23:49:53 GMT
ADD file:e3a6f7566ee3c2ba61d27d801d3522e045a4be64a42f32ee52d933b68338d06f in / 
# Wed, 16 Dec 2020 23:49:55 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 07:52:08 GMT
RUN set -ex     && apk add --no-cache ca-certificates
# Thu, 17 Dec 2020 07:52:09 GMT
COPY file:29c6c1625420a558a03cc7ed253192f8138cba6212b64e30217fb6488af668e2 in /bin/registry 
# Thu, 17 Dec 2020 07:52:10 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 17 Dec 2020 07:52:12 GMT
VOLUME [/var/lib/registry]
# Thu, 17 Dec 2020 07:52:13 GMT
EXPOSE 5000
# Thu, 17 Dec 2020 07:52:14 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 17 Dec 2020 07:52:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Dec 2020 07:52:16 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:56fec67ad66eea034cf5b7d0d0ffd355c0fe87611bad132ac5a952fcaa52138b`  
		Last Modified: Wed, 16 Dec 2020 23:50:34 GMT  
		Size: 2.6 MB (2620769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf7cc14966ceb5e5b46be135c16f21f7af42f270518ed92962f9514d0874ce7d`  
		Last Modified: Thu, 17 Dec 2020 07:52:29 GMT  
		Size: 299.9 KB (299919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96618f9c1a201fedc2049c85c36fc0b4a817442c4f712140f49d76310034d2f7`  
		Last Modified: Thu, 17 Dec 2020 07:52:33 GMT  
		Size: 6.4 MB (6391083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5acb2c1463288a9621bede426350b5e343e6beb7639ab71ea9be3cd67599bb52`  
		Last Modified: Thu, 17 Dec 2020 07:52:28 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9b1ea70368acb9d8c55ea555a87c799805882309d54ad7af9aa7d8e1d8b366`  
		Last Modified: Thu, 17 Dec 2020 07:52:29 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.7.1` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:df3e5e623e469600373cb327e8788e4eeb5e4a4c48e58461feb2b0d4c7f3c588
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9265349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1525b096095b7c89c39f47897379a700ca4a56864a18fd60c35dbb46cbf4cb9a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Thu, 18 Jun 2020 17:40:29 GMT
RUN set -ex     && apk add --no-cache ca-certificates
# Thu, 18 Jun 2020 17:40:29 GMT
COPY file:51a441e6eceff49ef32609e7070b64e8d5690648e4f915cc825274e6fe37aed2 in /bin/registry 
# Thu, 18 Jun 2020 17:40:30 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 18 Jun 2020 17:40:31 GMT
VOLUME [/var/lib/registry]
# Thu, 18 Jun 2020 17:40:31 GMT
EXPOSE 5000
# Thu, 18 Jun 2020 17:40:32 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 18 Jun 2020 17:40:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Jun 2020 17:40:33 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e44ffe5a70335b9c005f5ce0f0fcbbebb301d9b6440409c5b868dabcd86c9ba`  
		Last Modified: Thu, 18 Jun 2020 17:40:43 GMT  
		Size: 300.1 KB (300114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc788ee7896b71758970563ffa9bd4deb180dee6000984911138c49e9eba6a23`  
		Last Modified: Thu, 18 Jun 2020 17:40:45 GMT  
		Size: 6.2 MB (6240198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f89902f2529afb002c788b9e561f9798a8fe5ed45ab604447bb88e77528761bb`  
		Last Modified: Thu, 18 Jun 2020 17:40:44 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:215110f71eb42468d3edb51073d4e8e18bbdbd09c491a9b72240efeb4f6ec263`  
		Last Modified: Thu, 18 Jun 2020 17:40:44 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `registry:latest`

```console
$ docker pull registry@sha256:9bd4d195c5daf7abf4703e36e0c1423181ad6de9f06d737c61bb33610fb8b585
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `registry:latest` - linux; amd64

```console
$ docker pull registry@sha256:e09ed8c6c837d366a501f15dcb47939bbbb6242bf3886270834e2a0fa1555234
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9937424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d4f4b5309b1e41b4f83ae59b44df6d673ef44433c734b14c1c103ebca82c116`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Thu, 18 Jun 2020 18:20:04 GMT
RUN set -ex     && apk add --no-cache ca-certificates
# Thu, 18 Jun 2020 18:20:04 GMT
COPY file:21256ff7df5369f7ad2e19c6d020a644303aded200bdbec4d46648f38d55df78 in /bin/registry 
# Thu, 18 Jun 2020 18:20:04 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 18 Jun 2020 18:20:04 GMT
VOLUME [/var/lib/registry]
# Thu, 18 Jun 2020 18:20:05 GMT
EXPOSE 5000
# Thu, 18 Jun 2020 18:20:05 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 18 Jun 2020 18:20:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Jun 2020 18:20:05 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47112e65547dd36dc84ab7aac240f297c424b449d78335758620967bed8ea845`  
		Last Modified: Thu, 18 Jun 2020 18:20:13 GMT  
		Size: 299.6 KB (299598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46bcb632e50679325611e71844537bebdb70fc1bf9021e052d783088477322c4`  
		Last Modified: Thu, 18 Jun 2020 18:20:14 GMT  
		Size: 6.8 MB (6823927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1cc712bcecda5c187b281d8452745a2593f4dedda30a4bc32b49263e81e5bc6`  
		Last Modified: Thu, 18 Jun 2020 18:20:12 GMT  
		Size: 370.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3db6272dcbfa9e8cb78cf93f1119d2c4960b628623d7c077ddd97047613468ff`  
		Last Modified: Thu, 18 Jun 2020 18:20:13 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:latest` - linux; arm variant v6

```console
$ docker pull registry@sha256:c8c97b4d572c33156da59bae82f6b833abf5ceaa69bb18d002406c2891fce4a8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9312382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2126abe3746bfb8bd3bccc38ecc00d331a3bad9db38232c473ddf04e92c2078a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 16 Dec 2020 23:49:53 GMT
ADD file:e3a6f7566ee3c2ba61d27d801d3522e045a4be64a42f32ee52d933b68338d06f in / 
# Wed, 16 Dec 2020 23:49:55 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 07:52:08 GMT
RUN set -ex     && apk add --no-cache ca-certificates
# Thu, 17 Dec 2020 07:52:09 GMT
COPY file:29c6c1625420a558a03cc7ed253192f8138cba6212b64e30217fb6488af668e2 in /bin/registry 
# Thu, 17 Dec 2020 07:52:10 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 17 Dec 2020 07:52:12 GMT
VOLUME [/var/lib/registry]
# Thu, 17 Dec 2020 07:52:13 GMT
EXPOSE 5000
# Thu, 17 Dec 2020 07:52:14 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 17 Dec 2020 07:52:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Dec 2020 07:52:16 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:56fec67ad66eea034cf5b7d0d0ffd355c0fe87611bad132ac5a952fcaa52138b`  
		Last Modified: Wed, 16 Dec 2020 23:50:34 GMT  
		Size: 2.6 MB (2620769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf7cc14966ceb5e5b46be135c16f21f7af42f270518ed92962f9514d0874ce7d`  
		Last Modified: Thu, 17 Dec 2020 07:52:29 GMT  
		Size: 299.9 KB (299919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96618f9c1a201fedc2049c85c36fc0b4a817442c4f712140f49d76310034d2f7`  
		Last Modified: Thu, 17 Dec 2020 07:52:33 GMT  
		Size: 6.4 MB (6391083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5acb2c1463288a9621bede426350b5e343e6beb7639ab71ea9be3cd67599bb52`  
		Last Modified: Thu, 17 Dec 2020 07:52:28 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9b1ea70368acb9d8c55ea555a87c799805882309d54ad7af9aa7d8e1d8b366`  
		Last Modified: Thu, 17 Dec 2020 07:52:29 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:latest` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:df3e5e623e469600373cb327e8788e4eeb5e4a4c48e58461feb2b0d4c7f3c588
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9265349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1525b096095b7c89c39f47897379a700ca4a56864a18fd60c35dbb46cbf4cb9a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Thu, 18 Jun 2020 17:40:29 GMT
RUN set -ex     && apk add --no-cache ca-certificates
# Thu, 18 Jun 2020 17:40:29 GMT
COPY file:51a441e6eceff49ef32609e7070b64e8d5690648e4f915cc825274e6fe37aed2 in /bin/registry 
# Thu, 18 Jun 2020 17:40:30 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 18 Jun 2020 17:40:31 GMT
VOLUME [/var/lib/registry]
# Thu, 18 Jun 2020 17:40:31 GMT
EXPOSE 5000
# Thu, 18 Jun 2020 17:40:32 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 18 Jun 2020 17:40:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Jun 2020 17:40:33 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e44ffe5a70335b9c005f5ce0f0fcbbebb301d9b6440409c5b868dabcd86c9ba`  
		Last Modified: Thu, 18 Jun 2020 17:40:43 GMT  
		Size: 300.1 KB (300114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc788ee7896b71758970563ffa9bd4deb180dee6000984911138c49e9eba6a23`  
		Last Modified: Thu, 18 Jun 2020 17:40:45 GMT  
		Size: 6.2 MB (6240198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f89902f2529afb002c788b9e561f9798a8fe5ed45ab604447bb88e77528761bb`  
		Last Modified: Thu, 18 Jun 2020 17:40:44 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:215110f71eb42468d3edb51073d4e8e18bbdbd09c491a9b72240efeb4f6ec263`  
		Last Modified: Thu, 18 Jun 2020 17:40:44 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
