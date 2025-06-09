## `clojure:temurin-24-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:dd7a266c454e160493e65d76cced610ea1453397f3419df71644ed8710bc8edd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:3e6c48621753d2535bf8f5e8e072aee9da555416d6ca959a831fe57ac576ac8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.1 MB (213113072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aabb78e53095868041d6a8970367159d0f685ae833d34108663b021f335d26d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:54107f2de180b7b6e9f909d2f1c6c18e10c700a6bd80a035d931768b06bb2905`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 53.8 MB (53750195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ae8ac4853aaa42d1d61553335ced11256e4b2093a7b1efb42e69714b210f5f`  
		Last Modified: Mon, 09 Jun 2025 19:20:32 GMT  
		Size: 90.0 MB (89952019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a135e89bc4430bd38dfdfe819be98704bee21a6d50ddc8d7c0ab9b28ccf2fc40`  
		Last Modified: Mon, 09 Jun 2025 19:20:33 GMT  
		Size: 69.4 MB (69409819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21306ae107ff46ace3f078db2a72348bd2adff008eedbbca19b7fc9e579dbec9`  
		Last Modified: Mon, 09 Jun 2025 19:20:24 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0cf0aa2f3748b401b8a2f7871b5305e600bee99be2a64306094e26ba1b17595`  
		Last Modified: Mon, 09 Jun 2025 19:20:25 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:ce934c21098cde3512740874892a7a12a9c122d7441c918339fd00f265193ba1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7363722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cb55afc4947624f7487a308afea0d8ffa2fa5f3c0deec3a76c3d943f63cea32`

```dockerfile
```

-	Layers:
	-	`sha256:95c2efd9c377f25ec7b274ace93d49b48ae9c7ea6432d87a931fe54194127eb7`  
		Last Modified: Mon, 09 Jun 2025 18:41:07 GMT  
		Size: 7.3 MB (7347908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32c2e9cd7dacf244752f02fd52349b64ae821628502eef5872f7b1e0b8df624b`  
		Last Modified: Mon, 09 Jun 2025 18:41:08 GMT  
		Size: 15.8 KB (15814 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4965b6b8fc93ff721b00dd488c1dd3a49ae374cfba1389f32685e1084e3ffacc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.9 MB (210877830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:103680a164aac4a766f4b0b24fd67bea64ad4bbe19f7f7a6e7cadef2ba73907b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b2737025fe8da5b868f566cb4e3dc3330028cee06c83db854f56467eca6e09b8`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 52.2 MB (52247755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e138a1071d10d13cb8382959f5fbc892b4601755504e76a2d09f248081aa2606`  
		Last Modified: Fri, 06 Jun 2025 02:47:11 GMT  
		Size: 89.1 MB (89091274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce5a03a43022867c8f473f19981e940734437d6aa22a72a1b48c4b8570bc05c2`  
		Last Modified: Mon, 09 Jun 2025 18:00:09 GMT  
		Size: 69.5 MB (69537761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d5da1b9571251fc4d4e00d3ccd34a8fe125a13e8149771bbe4bc951c3bfe6d`  
		Last Modified: Mon, 09 Jun 2025 17:59:49 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37285717d4447a47d6c3eb0459e75b67156d25a8c492764402b5d43da84f3114`  
		Last Modified: Mon, 09 Jun 2025 17:59:49 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:60445cb177e2a239576f28e5c32eb43893700779aff26badd6dc784ad98e0fbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7368936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f78fb0be888aa1d386c4245015131d98ef4d86b05d8c02a5ea4c538dfc919915`

```dockerfile
```

-	Layers:
	-	`sha256:b62883be3848da3fbfc5b0f299dc02e24a28becfa2dbf5d91041f1ba680116aa`  
		Last Modified: Mon, 09 Jun 2025 18:41:14 GMT  
		Size: 7.4 MB (7353004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:266414f67d6d9395bd2a9e7c1e5f456d4ec604af1370a238f8759dd28b44bca0`  
		Last Modified: Mon, 09 Jun 2025 18:41:14 GMT  
		Size: 15.9 KB (15932 bytes)  
		MIME: application/vnd.in-toto+json
