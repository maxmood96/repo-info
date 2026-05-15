## `clojure:temurin-8-trixie`

```console
$ docker pull clojure@sha256:e073f71be88108bc272c8299856589327c6206f2bca1040bb53f22874adb9a2a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:cb8bb26a6d16ca96497eac0b3d7a5b0d47a7bc8b9e018bf550ceb830bf624f44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.1 MB (190105194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c981d643a96370a8d4ecaf2d0e5a27b03338a3b43c7c3221619eed7bb55e426a`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 15 May 2026 20:13:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:13:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:13:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:13:38 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:13:39 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:13:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:13:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:13:55 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:307f8152a55ef1e9eeb1acbbee7bc81232615329eaeb00d8dd93b46be297f34c`  
		Last Modified: Fri, 08 May 2026 18:24:07 GMT  
		Size: 49.3 MB (49302320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a11122bdd289b518326a713fa533298d46cc425e181e542f29a369c1ae713485`  
		Last Modified: Fri, 15 May 2026 20:14:16 GMT  
		Size: 55.2 MB (55198701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:625fd256c627e3f828d79a5ce00af16e2b94df0c6325bfde3505f3efb7a6916f`  
		Last Modified: Fri, 15 May 2026 20:14:16 GMT  
		Size: 85.6 MB (85603526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aebc3e1c7cf4843c1c1ed3ced2ccc900dd0aba5c5547ede074c004999036193`  
		Last Modified: Fri, 15 May 2026 20:14:13 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:dea451e884b6932bb136802e78db712daa89879b4c1097f87f0f32cf413adce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7606066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb8d414eb01950711c0010194a2d9b37a35c6b878a63cb33ace54b1bf6fb7a0e`

```dockerfile
```

-	Layers:
	-	`sha256:4f0a99ba6d83d5c95211ec5db1f2e8fd3c24bbc09a54a1bbbf683e70beddc571`  
		Last Modified: Fri, 15 May 2026 20:14:14 GMT  
		Size: 7.6 MB (7591742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4db8b2b46e5052dfe4dd2242e029518e1806b5a06223b75ecf44e1c4c4d1683f`  
		Last Modified: Fri, 15 May 2026 20:14:13 GMT  
		Size: 14.3 KB (14324 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2c8bea2efcbbc06faafa4cd0a884017e09d6bebf8dd712e07d758d22cd4b361b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.4 MB (189358570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46974d24da17009f78c87fba1294c31153602669344ecb78fcae971207aefef4`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 15 May 2026 20:13:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:13:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:13:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:13:38 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:13:38 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:13:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:13:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:13:56 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b5d74b688654dda99557234223479d1600781c2797759908abb12a2e782ab1ad`  
		Last Modified: Fri, 08 May 2026 18:26:51 GMT  
		Size: 49.7 MB (49669445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2aa41ad5f8a87f62ce857ec97728ab3edfaa1e10cc62db29b3ee1cfd5b5d3f`  
		Last Modified: Fri, 15 May 2026 20:14:16 GMT  
		Size: 54.3 MB (54272936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f26092560c99b94cf59e0262b880828253f9c006b33391e683a3314c4130ce`  
		Last Modified: Fri, 15 May 2026 20:14:16 GMT  
		Size: 85.4 MB (85415542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e74b7e3fef3324c4570de014446ecbf4762f82f867b053ae8263561eed5f4c`  
		Last Modified: Fri, 15 May 2026 20:14:13 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:171bae0348c09e1b37803c3c1fe58718aaeefc28ea10591299a157434a5638e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7613914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abcbbcc98973a502ffd173deb076670b36edbacae85fdaad202a6691917cd513`

```dockerfile
```

-	Layers:
	-	`sha256:d2a7418cbe864b1554bde30be98d5aa3679897e59117c0dfff4985bac81cc9c8`  
		Last Modified: Fri, 15 May 2026 20:14:14 GMT  
		Size: 7.6 MB (7599472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:080bcaa7ea799be8f443f0803da7db8428b1ab2b7948f7fc65a4bffc2a3d390f`  
		Last Modified: Fri, 15 May 2026 20:14:13 GMT  
		Size: 14.4 KB (14442 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:c1ea02850e0c7feb6ce99c273f1a0338cddb053d87c4b0a13d762886768128ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.8 MB (196800667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0558c4db15453f69d96ae0a2caccfe6e568d2ed8c4d743b4e2da3f4656a39df`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Tue, 12 May 2026 21:49:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:49:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 12 May 2026 21:49:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:49:10 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Tue, 12 May 2026 21:49:11 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:16:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:16:17 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:16:17 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:95ea8643a6311b39c5ca6b858ab22e7e7fb5819831b6070e3d6390a0ebf1be97`  
		Last Modified: Fri, 08 May 2026 19:46:54 GMT  
		Size: 53.1 MB (53123165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6108e5c2a2245ec0c51d22b23687faec2598356811a7675057929aac5f8deda`  
		Last Modified: Tue, 12 May 2026 21:50:14 GMT  
		Size: 52.7 MB (52669152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d894f23c35ded210607bbba85ccd32808b67532cf04e223c971628f7e37d5bbe`  
		Last Modified: Fri, 15 May 2026 20:17:02 GMT  
		Size: 91.0 MB (91007703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8689be0370b603ad61fc9731599f850a804cf068dbc7faa882ded25326e186e7`  
		Last Modified: Fri, 15 May 2026 20:16:58 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:0c78a67afa8781cc3e54e2822447ab78d633ffad2c102b37be82530180c3670f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7611130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:641db89b29787f8e689b48d0ad00c7014e66bc8438ddb9cd890ffe7c3693f140`

```dockerfile
```

-	Layers:
	-	`sha256:889e51f4eadd546b70ef660c04f6618523e86d1c9bd60b5721e93d7a3843b78a`  
		Last Modified: Fri, 15 May 2026 20:16:59 GMT  
		Size: 7.6 MB (7596758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c79bc5b9a16b9df775906addd2c74f774ae54a0d068337583bc6ea9fdcecf04`  
		Last Modified: Fri, 15 May 2026 20:16:58 GMT  
		Size: 14.4 KB (14372 bytes)  
		MIME: application/vnd.in-toto+json
