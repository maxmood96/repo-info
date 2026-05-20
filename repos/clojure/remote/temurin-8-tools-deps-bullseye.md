## `clojure:temurin-8-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:47676aa58b9d394c6c8321120984bd916b90e93e66c376a1681e5420bbf19f91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:cca83bf0f2aafbed64ec6030d314747bb283329046f78e0205c002c3610bb9aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.6 MB (178570115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98bf470272a69ce684f983df56ce52a913e5186d9e20affe80972f2d1ae3539b`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1779062400'
# Tue, 19 May 2026 23:55:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 May 2026 23:55:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 19 May 2026 23:55:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:55:52 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Tue, 19 May 2026 23:55:52 GMT
WORKDIR /tmp
# Tue, 19 May 2026 23:56:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 19 May 2026 23:56:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 19 May 2026 23:56:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d0d98eecfa3b5c942eada879fdb4cf6f79f0b9612ede79322d9d16fc3e984ee0`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 53.8 MB (53768852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c11f354c52fee25aadb5a6764dc022b3c95a0893a699a0846e4f0e4be5f782`  
		Last Modified: Tue, 19 May 2026 23:56:20 GMT  
		Size: 55.2 MB (55198706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f77336069bdaf06d07c100eeda8ff4f8e49fa59579ce0f378fa4aa0db39aa26`  
		Last Modified: Tue, 19 May 2026 23:57:02 GMT  
		Size: 69.6 MB (69601912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6acea9d288b57210162a24a73b0b1ac258cd0558b73e49ec7fc9457ed1501b6`  
		Last Modified: Tue, 19 May 2026 23:57:00 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:e38fb3752500c45c98efb07a5c36135b6be9614e0455ae899cc1a6a0b48beccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7542032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:400a75ddf9a5357800aaad84b8711d4b84ff6bef5f762b636f9e9329325fe278`

```dockerfile
```

-	Layers:
	-	`sha256:f45f273f2ebd41ba6e8b510b028bc039a12748cfbcf6958b962b7e5e4cf348f3`  
		Last Modified: Tue, 19 May 2026 23:57:01 GMT  
		Size: 7.5 MB (7528638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bc7d89fe13fe1438f5a1b7012d2e807c47e534288e4ff52e669ddc072a53108`  
		Last Modified: Tue, 19 May 2026 23:57:00 GMT  
		Size: 13.4 KB (13394 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d03365e91259a211a31281b848d3147c3ea764a8be47013f3485f7b5151064bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.3 MB (176301114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a39957e5d6b4d3606043eff78c93568417e742d7faac3f36ff82c6772fc6ef1b`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1779062400'
# Wed, 20 May 2026 00:03:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:03:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:03:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:03:53 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 00:03:53 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:04:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 00:04:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 00:04:06 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9f08527663b6ddbac974253d3632db7fd8c400d9acb6601fc251de137ec53a8e`  
		Last Modified: Tue, 19 May 2026 22:36:30 GMT  
		Size: 52.3 MB (52256578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc2ab707aaace09a876aae0c3c6baadd0f1d3ac2f454a3044922b8c7d816019`  
		Last Modified: Wed, 20 May 2026 00:04:24 GMT  
		Size: 54.3 MB (54272922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11bc8e8a9c48fd895f891937313341a01f044e54614f152c7d79717471a61e34`  
		Last Modified: Wed, 20 May 2026 00:04:25 GMT  
		Size: 69.8 MB (69770968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae145b1dadccd7ca029fc0353e2b2adfab7266dde1e7c3e0fc272236b054b089`  
		Last Modified: Wed, 20 May 2026 00:04:21 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:b2a6c0118ae14433f8b0c2403559e968861ba0fdd51d5588a8c0e3565934ec32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7548903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd890dbaddb7458ef53dacdc372d24652fd80853de02c261f364f24c40476701`

```dockerfile
```

-	Layers:
	-	`sha256:8867da58226c5a92e6d11a35bc07a1c8d7e7357a4ca44910cabc437603f2b6e1`  
		Last Modified: Wed, 20 May 2026 00:04:22 GMT  
		Size: 7.5 MB (7534437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e804c1a993848a0fdfe139fc031f7b2684ee41caf59689c26402dc9e16394c6d`  
		Last Modified: Wed, 20 May 2026 00:04:21 GMT  
		Size: 14.5 KB (14466 bytes)  
		MIME: application/vnd.in-toto+json
