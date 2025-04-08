## `clojure:temurin-21-tools-deps`

```console
$ docker pull clojure@sha256:a8ba5723a2f37285192c5cdd5bd759a879baca203ef8fe152cd1dbf09b39c237
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps` - linux; amd64

```console
$ docker pull clojure@sha256:0af9081be70a515de63d50eec01e0ae988e0b96383a87e33df091761f29e465c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.1 MB (287071509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a756815530f4b5fc97a98f14deb396ffd0ec1259ab3532d2e244d39f6c0f938f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:23b7d26ef1d294256da0d70ce374277b9aab5ca683015073316005cb63d33849`  
		Last Modified: Tue, 08 Apr 2025 00:22:55 GMT  
		Size: 48.5 MB (48490541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b1fd165db7e0b1679d6c0deee1aaa0894b7caee3e9f955f7d2212716ba7a31`  
		Last Modified: Tue, 08 Apr 2025 01:36:41 GMT  
		Size: 157.6 MB (157585889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c076b755c8acf819c71e133466b88b3993dc98480f38b839e89344d6134a6e6`  
		Last Modified: Tue, 08 Apr 2025 01:36:41 GMT  
		Size: 81.0 MB (80994036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557e5e9916e971674896561e85a460bb034193ff24098f9af88e16af694f88d7`  
		Last Modified: Tue, 08 Apr 2025 01:36:37 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e51588b5bc52729994a05936c3c7107b97512c08528d5a52a0da48a15ccdcfd2`  
		Last Modified: Tue, 08 Apr 2025 01:36:37 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:02c92c628f18bee59fab4841c22fddd25ea2e7ffc9f35e6e279e8dd282132a59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7195398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:870d9066a070590f673e43a0cb6f79cb36e77bdc992e510ebcfaa633182ebc27`

```dockerfile
```

-	Layers:
	-	`sha256:11fdf377efc21fba7fb99f9f09ddfc1ea17a67e7164acefa064c1c450fab3bde`  
		Last Modified: Tue, 08 Apr 2025 01:36:38 GMT  
		Size: 7.2 MB (7177578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46490261aa3cde3786f49a72e62c24577139c113866d2c4367c0afa63a03ab87`  
		Last Modified: Tue, 08 Apr 2025 01:36:37 GMT  
		Size: 17.8 KB (17820 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b27070d5fba67237683abfd4e4883109683e1731364af192407f025d0eeb2b0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.0 MB (285007760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dd0efdeed5d28346be9e4b121303e07c1a530ac24379ebff69d1fca8b90d8d8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 08 Mar 2025 19:45:48 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Sat, 08 Mar 2025 19:45:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Mar 2025 19:45:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Mar 2025 19:45:48 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Sat, 08 Mar 2025 19:45:48 GMT
WORKDIR /tmp
# Sat, 08 Mar 2025 19:45:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Mar 2025 19:45:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:545aa82ec479fb0ff3a196141d43d14e5ab1bd1098048223bfd21e505b70581f`  
		Last Modified: Mon, 17 Mar 2025 22:17:15 GMT  
		Size: 48.3 MB (48304855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeefa516d3f68b625053d7ffc6bf700f8016157a685ab86fe0d07456ee280936`  
		Last Modified: Mon, 17 Mar 2025 23:51:25 GMT  
		Size: 155.9 MB (155859256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249b3c3c22a5cadb196da1a98f3d956cd16310fdbf248ea5e6d7d1298512304e`  
		Last Modified: Mon, 17 Mar 2025 23:51:24 GMT  
		Size: 80.8 MB (80842609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc8e1c2fc5ec575b8284ad34beef2fee8f2c0bd127e993b9b1e975e4d489928`  
		Last Modified: Mon, 17 Mar 2025 23:51:22 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecddc602048c38589863089c44bed07922e3a18e312c745efdc1da973e2cafc5`  
		Last Modified: Mon, 17 Mar 2025 23:51:22 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:45ee215c8a9a9602a10b5a7d6e37a6980933d34b2884daa961036717f8cf467f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7200056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9660addf5796939e66d34da94a48c85223f45ab4a1b752a2111d95f5799a597a`

```dockerfile
```

-	Layers:
	-	`sha256:d9ea6cb43158598eb7889998111543f5fccf674ff6b6c9a0e70dcb83d773d6e4`  
		Last Modified: Mon, 17 Mar 2025 23:51:22 GMT  
		Size: 7.2 MB (7182045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a681e6a56e15e368ec4a4baa21413f75249b0f040ac7f94fd430e1199d20657`  
		Last Modified: Mon, 17 Mar 2025 23:51:22 GMT  
		Size: 18.0 KB (18011 bytes)  
		MIME: application/vnd.in-toto+json
