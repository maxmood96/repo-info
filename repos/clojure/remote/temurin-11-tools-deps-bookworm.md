## `clojure:temurin-11-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:6dc62c8de70402695b03f07776d8d400e080c3dde380f30ab2039c6abb9a2b43
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:3d6c6f7fdbc540ae434007fa752faab48ebd1e45c2ebc22a68fd19a930767c65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.1 MB (276116205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75416d35bca7405a9b0c102b42f3dec5887386ad1ac77bf8dc8d935f0029df2b`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc02d519527eb8c9b3469f3b1cb404ea5c0094d7355c8fd73c96f3f870bbb4e`  
		Last Modified: Tue, 12 Nov 2024 02:23:42 GMT  
		Size: 145.6 MB (145601329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c2e85ef2b50ff2c5794c2ce789ad2748ac51e60024e853cf301c176056cf9f`  
		Last Modified: Tue, 12 Nov 2024 02:23:43 GMT  
		Size: 80.9 MB (80938537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a89299a58597e1de3a84b9d5c84d6a10bfde8d05a6ee7c637f21e45218cc556e`  
		Last Modified: Tue, 12 Nov 2024 02:23:40 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f6592025c9f1a89208dc193fc5b3eca489e698dc4ca3c8583bef98885c0ef93d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7216844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aa01102bc1de04acdbce86f124bdc19fe433acee0f0386b00860f00729c9760`

```dockerfile
```

-	Layers:
	-	`sha256:96fd74c790d9b7f720fbcee928b85e28ea786d0b86dfd7fea0dc946c9802f44d`  
		Last Modified: Tue, 12 Nov 2024 02:23:40 GMT  
		Size: 7.2 MB (7202594 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d65d4c40f6c1981a2ede6d72b38ccf666594601b107020448032c681c9be5c8`  
		Last Modified: Tue, 12 Nov 2024 02:23:40 GMT  
		Size: 14.2 KB (14250 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4ae9f16179bbae4731cec637704e85d5d570d0922e3d49d4efabb6dfdc35cd5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.8 MB (272764790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7851cbd8f92975f43e428805248ecbe2ece41a1d78a421914ba138d5909cbb4b`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:887acec9ae8608e8242cc2712ca5110681b42182eb911e5fe3d78e161502ec12`  
		Last Modified: Thu, 24 Oct 2024 09:03:11 GMT  
		Size: 142.4 MB (142389122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b689cb2ac0ed8ed9b1f5d7f5864607d71364c9fb26c5b3de608e3fb121e888`  
		Last Modified: Thu, 24 Oct 2024 09:08:53 GMT  
		Size: 80.8 MB (80790046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39dc85ef66eb47bfb8742d6c437d0b55e8f826a3fd46399ab21911c9e7d5a04d`  
		Last Modified: Thu, 24 Oct 2024 09:08:51 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:2e317eff326493318c6d7f8d0a39df7fc11646475c6c50f7d14967ee4df5616b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7223128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f6032694e3977a80b5b06e8138983e6d2163e8d07bb8af82cbd6fd2a2133f42`

```dockerfile
```

-	Layers:
	-	`sha256:8ccde8d875121c007dfa36773f9750cb689403739cca3c2b2539a7b20135404e`  
		Last Modified: Thu, 24 Oct 2024 09:08:51 GMT  
		Size: 7.2 MB (7208945 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a32ab0a2240e586198ec77c3ee75bbfaf35e397eb61c4df87019694139b83a3`  
		Last Modified: Thu, 24 Oct 2024 09:08:51 GMT  
		Size: 14.2 KB (14183 bytes)  
		MIME: application/vnd.in-toto+json
