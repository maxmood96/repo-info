## `clojure:temurin-8-tools-deps-1.12.1.1561-bullseye`

```console
$ docker pull clojure@sha256:ebef9238f71ee5fe8c235157e34b75b1895cf2db4d68424a73d9d52044ad932c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.1.1561-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:409c94eb2922d9141076c9d8a9d6a499c671a374f6ee0f31b6beaf2c4f1e5067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.9 MB (177948053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf54f1dbbf6fb0d61ecc02abeddbcf850c11c347cc0949b88e9fbfe6a75b5a03`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:078965fc7cf303b72cc4eef5479dc2dbf5bc84fb8e6052a89b9b5362e14b3651`  
		Last Modified: Tue, 12 Aug 2025 20:44:43 GMT  
		Size: 53.8 MB (53755344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae1b155119abc1772b581722d912428f48efa53937fcfeb9c1dbb71aa66be8c`  
		Last Modified: Mon, 18 Aug 2025 16:52:23 GMT  
		Size: 54.7 MB (54731348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1041938913c99d06f657db44cd17e462948e0c1f162f3a229c602d3f7eefb394`  
		Last Modified: Mon, 18 Aug 2025 16:52:21 GMT  
		Size: 69.5 MB (69460718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da04bf8635e99939fc53b05890a25a5dccae954f165a625a2e54dedfff6d490`  
		Last Modified: Mon, 18 Aug 2025 16:52:14 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.1.1561-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:7874d5f863d935b4513cb4a010409f5f05f9c02d124e21126e8506389c28f779
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7531513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d4b5a5f5447307d8d8739d2e851c50f059d7b2fe8c8572ac89e8a154b5e28d2`

```dockerfile
```

-	Layers:
	-	`sha256:ee25f0bee1fc9c39397eef48d8a4fea1896bce2801e7b121f3cc9fdd8b0fd61b`  
		Last Modified: Mon, 18 Aug 2025 18:44:43 GMT  
		Size: 7.5 MB (7517277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a9f41d865a4ccd14145ba89413703189e4a8cf95c73e8545be876fbca2ee8ca`  
		Last Modified: Mon, 18 Aug 2025 18:44:44 GMT  
		Size: 14.2 KB (14236 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.1.1561-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c0ac5b9b686a465b2812cc934270745063670c7452108d200134904d45169245
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.7 MB (175672975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b0d363a873d28056c84134c94230c2d02bce4453c2fdba929c91b63edcc99b2`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7b68ea47bc3cd8615e51fdbe0976cb4999ba56ce8764e755543a4521d69a32f6`  
		Last Modified: Tue, 12 Aug 2025 22:08:57 GMT  
		Size: 52.2 MB (52248409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c68418c918156697c68aa13e1642c98a2beeadf9646a706b7123bd36165147`  
		Last Modified: Mon, 18 Aug 2025 16:54:18 GMT  
		Size: 53.8 MB (53835632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3506b08db327ee84b62bcd421c5b32c936095457856238da51da2e961cf0f19d`  
		Last Modified: Mon, 18 Aug 2025 16:54:22 GMT  
		Size: 69.6 MB (69588288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03fb9fa8c737a8cf0c082c3ba975135ce335aac7dddea4b6bce2fdbd7b5442f5`  
		Last Modified: Mon, 18 Aug 2025 16:54:05 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.1.1561-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:cfb480eb99e08155748b6e76a05f705620032a2c12773129573cfa53b043c813
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7537428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcb14ff320227bbcd91c5b3969fe4f209fa91a3829a2c77ded11d9509521864d`

```dockerfile
```

-	Layers:
	-	`sha256:dde60100ed1c45077d286526c75e438cc907f062890ec7882904546fef4bdb23`  
		Last Modified: Mon, 18 Aug 2025 18:44:50 GMT  
		Size: 7.5 MB (7523074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07a86c60155d1d9de8a99b49025ebda948b7e42c66d70c6b6c70b2085ac08375`  
		Last Modified: Mon, 18 Aug 2025 18:44:51 GMT  
		Size: 14.4 KB (14354 bytes)  
		MIME: application/vnd.in-toto+json
