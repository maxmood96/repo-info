## `clojure:temurin-11-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:c5366425af4a30e4c70dd39715b5d1f00f6d3e082013a5eec2c75e9e54ce9195
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:1df91b744874128842cd67d66c0f5b42e6422a7a5f70230d0f6fa6bc53c21db1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235069695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a243fbc4334086bcd99823f990cd5e7a0a6314321ffcf67a347298bc5bb01d85`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 00:54:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:54:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:54:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:54:31 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 00:54:31 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:54:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 00:54:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 00:54:45 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:cf5f39ef3fca9730ed04aee5f10040ea152a9793dec0d626f4205eeac5ec3fc0`  
		Last Modified: Tue, 04 Nov 2025 00:13:10 GMT  
		Size: 30.3 MB (30258596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a5d5bc916a6c0bf406b4c9fd70dc0d8b13c098bb279a20648ee1a9a41b0330`  
		Last Modified: Tue, 04 Nov 2025 17:43:51 GMT  
		Size: 145.7 MB (145658308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6e0049745f712aed8d0cefd2c39a89a9a58458290b7478ab4643b981e39cc5`  
		Last Modified: Tue, 04 Nov 2025 00:55:23 GMT  
		Size: 59.2 MB (59152148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce73cbf624a39e1741b6ed5f1fd8c9a5fb2d52117dcd5f22629b9911210f1f4d`  
		Last Modified: Tue, 04 Nov 2025 00:55:12 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:43c7f78421ec80537fcbe85f134e923bfc3e2f726294605d055c16c247969b4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5342475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb877e166c3565608248f3e7470b8dee2249a857b7886f19a263c3cc53e49383`

```dockerfile
```

-	Layers:
	-	`sha256:faeba095f699f220b69d2aed19556fe2d6288a024fed7f9434fc9dc81dcb6c0b`  
		Last Modified: Tue, 04 Nov 2025 10:36:31 GMT  
		Size: 5.3 MB (5328208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:081d1061e2d3c2a42c224101ce265aefcaec745ef86c68a58d3ea4cb872a3b8f`  
		Last Modified: Tue, 04 Nov 2025 10:36:32 GMT  
		Size: 14.3 KB (14267 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:223fb20f1fb7f6d8697b66653edb6020434e14c8eb98c44df0dba37138f95a32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230497397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1046154cb80d1540f3fa81982f956e07dccdcd5c918f6902f95131cc352e4c9`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 00:55:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:55:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:55:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:55:04 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 00:55:04 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:55:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 00:55:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 00:55:18 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:241077dc995c26590e89ca59e622bf97509f2613a9e84e3e745225e4259eb511`  
		Last Modified: Tue, 04 Nov 2025 00:13:03 GMT  
		Size: 28.7 MB (28748552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c90fe59719a7ff739fe21e44c037d6dc7360911f33b43f3f9c99f68c925655af`  
		Last Modified: Tue, 04 Nov 2025 00:55:39 GMT  
		Size: 142.5 MB (142460584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42dfbc695449bcfae84b8ff17a5cb65409522461a17ac9bd4fa58e3b3b6d0b0`  
		Last Modified: Tue, 04 Nov 2025 00:55:53 GMT  
		Size: 59.3 MB (59287618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c44735603884995feb47590f86d2f2d366f344ca9b7d94f89cb62b43b453a59`  
		Last Modified: Tue, 04 Nov 2025 00:55:44 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ddd3ff3fed83c32db0ae43dda55b9cce8207cac940fc3b4ad88cf70e7959b342
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5348943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5bcada269dea6d789ba2a12ed46f52779e9dc99a06daf0ea234414d767cb0a1`

```dockerfile
```

-	Layers:
	-	`sha256:1f089d5f5bf0523214e4bfee1a6edb564bc3def6e30df0a01391920826b6a45e`  
		Last Modified: Tue, 04 Nov 2025 10:38:05 GMT  
		Size: 5.3 MB (5334558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ed15d54709740b72982193721feb4d9062113a62b79c3dde01a6337253edc24`  
		Last Modified: Tue, 04 Nov 2025 10:38:06 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json
