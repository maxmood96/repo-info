## `clojure:temurin-21-bookworm`

```console
$ docker pull clojure@sha256:652949ae58c57780739a40c849c5cf0c1de8af156e0203c2f07b7339464fa4cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:ec573ccbc89443e0b1f8a50485b0656934d38a04a378ba18c07c94dac6b3fd1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.1 MB (288083765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e74126a30d14a62ec4b48a8e35a04013970e6ca027a237a0af80174ecea35b3f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d456ecc711ecd6f4598460dd07513722ca01ae080103586d3f4b078e92a9ad64`  
		Last Modified: Sat, 16 Nov 2024 03:51:46 GMT  
		Size: 157.6 MB (157568675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39fe833e47b042e40a7c67730166e55b4689beb8d309e4b854ea0ad6de455dad`  
		Last Modified: Sat, 16 Nov 2024 03:51:49 GMT  
		Size: 80.9 MB (80938354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:656d7b10d0a4c8506c1d638b07229a18bb8dd96afd010019d8103eea117181a8`  
		Last Modified: Sat, 16 Nov 2024 03:51:46 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580e016e303dcd7747db911f744f715bf790192e26fa8e50dc1a1581b503d5a9`  
		Last Modified: Sat, 16 Nov 2024 03:51:45 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:1b3f21d463a6db1441181fa1e8d973bf9a1e46fd05d8c24e3e6f97f1e1043efe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7205351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc7a42c84435e63db9e4b093841c24bc097da520c43ef15adcf4260963775d50`

```dockerfile
```

-	Layers:
	-	`sha256:0ef2280c9ec78f109f46fe2609f6fda99c09abfb9efb8d5a765770917dd8838b`  
		Last Modified: Sat, 16 Nov 2024 03:51:48 GMT  
		Size: 7.2 MB (7187530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4665e5fb76626ae2416129244ad4e9b377e42bf962dea876caf50a314a1caf99`  
		Last Modified: Sat, 16 Nov 2024 03:51:47 GMT  
		Size: 17.8 KB (17821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6e0a87bbe9d826843ec20857c388901a1145105405e64aeeee92fe4c3573a515
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.2 MB (286179450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:546be9c0b6706e8906a1e378598ccd07d310e5dcd1736cd5ba3df262b1722b4a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1a3f1864ec54b1398987bbe673e93d8b09842ecd51e86ab87d64857b70d188b1`  
		Last Modified: Tue, 12 Nov 2024 00:56:20 GMT  
		Size: 49.6 MB (49587201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ac2cdaa8d620e3458e01b043a2de8dec93076a8e68d2219825a903a144f593f`  
		Last Modified: Sat, 16 Nov 2024 05:10:03 GMT  
		Size: 155.8 MB (155793069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650009f935aecfe6e7a64d069a2b1126c9a32c37fc319095b838a1c4d17f3632`  
		Last Modified: Sat, 16 Nov 2024 05:42:14 GMT  
		Size: 80.8 MB (80798141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11189ef6d83473d6c9f2ada869fcbd3512329860ff9d47785ca1ba7c36240dd0`  
		Last Modified: Sat, 16 Nov 2024 05:42:12 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd428a1e3b4b8b8a88dd41b49f703db36af776f7ff49b7c45f6c83a3115d2180`  
		Last Modified: Sat, 16 Nov 2024 05:42:12 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:ea261b865344e9798e397a9b07951f31cdb070a8dab99a17167090ac3b2ba49f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7211381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e15f888465d4a6a2561e8c6535a17475c7a395ed004bacb6b7eab14c788ad12b`

```dockerfile
```

-	Layers:
	-	`sha256:09d6b556b0df936816ee0aaa190addef6aa561be3b26606f42f4eaa7aea282d8`  
		Last Modified: Sat, 16 Nov 2024 05:42:12 GMT  
		Size: 7.2 MB (7193370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56ae9f9a6f7cf18802f6491c49045a118838abcca367ddbca002c1b460542e40`  
		Last Modified: Sat, 16 Nov 2024 05:42:12 GMT  
		Size: 18.0 KB (18011 bytes)  
		MIME: application/vnd.in-toto+json
