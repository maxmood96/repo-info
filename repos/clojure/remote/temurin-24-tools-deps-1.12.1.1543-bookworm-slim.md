## `clojure:temurin-24-tools-deps-1.12.1.1543-bookworm-slim`

```console
$ docker pull clojure@sha256:4905721774e239e69b71bc92962c3b0125e1db15a83be2176c3e2e9f0b77ca18
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-24-tools-deps-1.12.1.1543-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:9255fa9c34ee51d9bfa12f3af24d3c29b5bf7d095502c283940d9dc239981591
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.7 MB (187707713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3059c1c07574ac30a990ed6732fa131c5331d373f116ebce72be7d19e1b04285`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f8263db77812641789651c2df70f53f3bfdf15790d0255092d0015a2573e1d`  
		Last Modified: Tue, 03 Jun 2025 22:37:28 GMT  
		Size: 90.0 MB (89951976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bea116b153af883189e17446488d855954b43c3792fbbd866358797a9b68a2f0`  
		Last Modified: Tue, 03 Jun 2025 22:37:27 GMT  
		Size: 69.5 MB (69529366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:870499f168c9d25e6708d6e4995be75ef1aaf86b630c81b3ffb4cc6602086043`  
		Last Modified: Tue, 03 Jun 2025 18:29:47 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3a6eca952f993cb1d7af8b3b826d797e48923ff0511e720aa97bdd34a395fb1`  
		Last Modified: Tue, 03 Jun 2025 18:29:52 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1543-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a851ff3e9a7a18431411e0463f429bfcdbcb385cd23a7adbaeb6242471424d68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4928016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7938e01c3f0ad3a34eaa086bf9588090fc952b7f8db6bcc9644d298a78317a35`

```dockerfile
```

-	Layers:
	-	`sha256:a3a16a9ae50e6ffb7e16981af0bb5df7058814f7b77a14f237e79b74f0f4ada0`  
		Last Modified: Tue, 03 Jun 2025 21:42:27 GMT  
		Size: 4.9 MB (4912144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b5e9473b270aad0444ca1f0dbe09bcc73e98a92597000869f0dc17b60166578`  
		Last Modified: Tue, 03 Jun 2025 21:42:27 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.1.1543-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d77050a15b3705d49fa3edb57ba4060610436bf9f66f14a0ad9b861ef383de30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.5 MB (186549168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:009f975f67df99772414a13b33d7b1c6867323685a705234a698e341cecada17`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e71e656269e61d9fee81d36b750f503dc64c9352c0276d046ba8584c69c03aa4`  
		Last Modified: Tue, 03 Jun 2025 11:05:45 GMT  
		Size: 89.1 MB (89091268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042f8e8d55e80b24f210450cfdd2a2fc9d5e23e3dde5ee05f485a7dd403b6dce`  
		Last Modified: Tue, 03 Jun 2025 18:53:19 GMT  
		Size: 69.4 MB (69391580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0343fe56fef9bc07f8a82efe17a67763e930c932df55794be00a2d4d2f4c397c`  
		Last Modified: Tue, 03 Jun 2025 18:53:09 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a18070bef44cff0d5650125fdd63031c3b6df6b379eff0eb4c4cbbdbee4484`  
		Last Modified: Tue, 03 Jun 2025 18:53:08 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1543-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:df97732f08917cbc8706920954f8b908e757a6c807ca47b2ab532352e3e8d5f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4933892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f931facafb7a1e109d43d8cca4866ad969159e574386f3dd84f5c11c28ab3b1`

```dockerfile
```

-	Layers:
	-	`sha256:c8fbd57191b1f83ed086e9293368a1ab62c5256a747328ee80f85b19feb6cbd4`  
		Last Modified: Tue, 03 Jun 2025 21:42:32 GMT  
		Size: 4.9 MB (4917902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0739ecc82e7c119f1e8abedfd207ac2e8bbecc71cc31f5f620ef29db1519e3ff`  
		Last Modified: Tue, 03 Jun 2025 21:42:33 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.1.1543-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:0ebae82a60fc37292e68145cac5add24851e4919c1f040c5d54fbf6b9dc0a6cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.3 MB (197334122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0adaf21fab3cb6f0464096f689c7209249fba6cdc4294b8435b7bb640c1fa11`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:701606535a7233566815cc9ad5f3e5853b443be5476286f6799008053dc2b03b`  
		Last Modified: Tue, 03 Jun 2025 13:39:02 GMT  
		Size: 32.1 MB (32066912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11812ef70a6e51874f7a3e88e70c2ad9b1a21e9929f025712f7e56568a7f3111`  
		Last Modified: Tue, 03 Jun 2025 09:27:03 GMT  
		Size: 89.9 MB (89920260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae07a2865f2723647b6fee9f20365f13e8aa5d4c8ffae0150b9fd9087150b8f8`  
		Last Modified: Tue, 03 Jun 2025 19:12:31 GMT  
		Size: 75.3 MB (75345908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cddca11ca79da36b897126177347969f070a24a79e912b28d9cd6a790bc5b9c9`  
		Last Modified: Tue, 03 Jun 2025 19:12:26 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f831dcb8e7cd8a23b410c02f10cadaf9a92359e72fb274f99355b77d15edc4ce`  
		Last Modified: Tue, 03 Jun 2025 19:15:53 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1543-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5c223a4e40208b7f1083d8f13ce7dcb5a160c2a8c7271fc65181807cdbf2dfc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4934520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0272d27dab3b4c456b1a8eba63c6bbdad8447b41b91676aefd5af30370a9743c`

```dockerfile
```

-	Layers:
	-	`sha256:fa297017d9d47ba5d33ad5e0c5e27220ad3242d94ac1759c74edae0fa3dbe0b1`  
		Last Modified: Tue, 03 Jun 2025 21:42:39 GMT  
		Size: 4.9 MB (4918600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bff0cc9cac9d855e079b3c1d17a940e91efdccb6a59ca70979055f7834f72f74`  
		Last Modified: Tue, 03 Jun 2025 21:42:40 GMT  
		Size: 15.9 KB (15920 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.1.1543-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:347bc7864e260b4bdda3df6b01f856b87626ca17f0b4556550b9c2ac3aa14b2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.4 MB (180434892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b362773a788784215a397a4d3a5c46f2ea27491d5567fb11f3aad84434970ba`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Tue, 03 Jun 2025 13:31:54 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b984f64a36288041a3c614f4a78a8680d1a70349b080261f6d6bd8de5660a8`  
		Last Modified: Tue, 03 Jun 2025 06:36:43 GMT  
		Size: 85.2 MB (85216876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:149f3e89f659661184f28ec2ffca2d54f2995ba19d636173287f8fa6e237e5e4`  
		Last Modified: Tue, 03 Jun 2025 18:44:22 GMT  
		Size: 68.3 MB (68334171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d15b243dd75693e805b8246534804adf8acc0bd764ff0645ea8d666e66710a9a`  
		Last Modified: Wed, 04 Jun 2025 04:19:16 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ae3c2ef3eb00b58f581b4803c85dda21fe52b2fa59cb5e6a0b85ebe4f3c306`  
		Last Modified: Wed, 04 Jun 2025 04:19:21 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1543-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:09d810c19f7c390d1435c62f8c1c6e31aa1ba721ee04a9bcbd1da63104c7ff8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4924777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9201478ba68b647f6b787b05f826af8d578e0c5be1e593a5b234d726b37d7c7`

```dockerfile
```

-	Layers:
	-	`sha256:615c41caf93584f3abe35d4d38ca7ff630573e1cbc3473dc45f048d7f213ac24`  
		Last Modified: Tue, 03 Jun 2025 21:42:45 GMT  
		Size: 4.9 MB (4908905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86a14ee87b8793c3725ba8ac04f1029bab6f7a9ebaafbdc86987987763bac29e`  
		Last Modified: Tue, 03 Jun 2025 21:42:45 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json
