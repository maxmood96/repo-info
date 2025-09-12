## `clojure:temurin-11-tools-deps-1.12.2.1565-bullseye`

```console
$ docker pull clojure@sha256:dcdea29e847cb6c771384fd4331d783cf7960bd3b75132c8d09fa64d9016e540
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.2.1565-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:1525d04a1e0aa10bd8a70c50453f4600e4f80cde89cefd96f0060ffd2bf988d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (268971295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3625ef607a03c0329aa911231ed6a821f3cd6d77cf2193d29d20017acaec1e81`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1757289600'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:035115815e46101f9c9956e02e706f2f3ec8748e2b415f0d232b51eb76a6a779`  
		Last Modified: Mon, 08 Sep 2025 21:12:56 GMT  
		Size: 53.8 MB (53755396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1a94c4845d642ed2cfbab29c831490d1890169c18099452bb2ed41c94e557fc`  
		Last Modified: Thu, 11 Sep 2025 02:26:26 GMT  
		Size: 145.7 MB (145658209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7f8d7d2aba20652b2b3f2b4032b366414b46f03dc85227f8fe337ef2809c92`  
		Last Modified: Thu, 11 Sep 2025 02:26:19 GMT  
		Size: 69.6 MB (69557045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86222a1ce7cfe114c5f97a3f612b012f6bffd81b5db95dd9ee44d2b01aa68d2`  
		Last Modified: Mon, 08 Sep 2025 23:01:47 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.2.1565-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:71952228b60ed0206563ffa3afb01dcb02c1f7aed571cf61edd331fcf407ccc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7430060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aba9af0f7c66ad9a2c282687a1094fc8f91a7626b5e52dc09d200c672657c9eb`

```dockerfile
```

-	Layers:
	-	`sha256:94bf22f628d691990c130691090675822cde639a983cc7bb6190f875371198b4`  
		Last Modified: Tue, 09 Sep 2025 00:35:32 GMT  
		Size: 7.4 MB (7415808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:deac7e8205f311e786578b10c20ab7b623b51a186b24eeae8d9de3da3be1ace2`  
		Last Modified: Tue, 09 Sep 2025 00:35:34 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.2.1565-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3e3da607213c75ac210e760f3b73700912b1a42ec0773c5b691e3dd2d53c99cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.4 MB (264392092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eec0a4c437124a855e4824111fe952957abbbfca9fda710aa607120db14726c8`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1757289600'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7df02cb4a974a4e8a9eb65ffcff7274f9dca341d29aaa763294c42e49805ca19`  
		Last Modified: Mon, 08 Sep 2025 21:15:41 GMT  
		Size: 52.2 MB (52248370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb45e08d097a3bc1bb3dc9b56b2dc5e2f4f86bf19063d12d777901f713a510b5`  
		Last Modified: Fri, 12 Sep 2025 03:14:40 GMT  
		Size: 142.5 MB (142459105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662e915296a9bf52305a474869c7c03b5b03455ef0cc9dd69163bad05a26da7b`  
		Last Modified: Fri, 12 Sep 2025 03:14:38 GMT  
		Size: 69.7 MB (69683972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:455db9d7a6c5b223d195f57a1fbb356ee8106567a30577afd8d0a835dd3357f6`  
		Last Modified: Tue, 09 Sep 2025 01:27:57 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.2.1565-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:0f9ec90ddf24a9f406fd20ab055c8fbfbecfdba0e8b4e484e3b27fbf1fd768aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7435894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f73ace82e05f4ea90d3d72398a50a74ab4278b1c3cf0a2cc784e040f671b6cd`

```dockerfile
```

-	Layers:
	-	`sha256:e2463eefd66340106de9a268ac1a54b521d194a52eaeab9076d0e6c3ee4fbceb`  
		Last Modified: Tue, 09 Sep 2025 03:35:32 GMT  
		Size: 7.4 MB (7421525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d36d21f9dccedfcbc90ebb97397dfe1bd16d6d3601bda6dbbc62c50a9321f9b`  
		Last Modified: Tue, 09 Sep 2025 03:35:33 GMT  
		Size: 14.4 KB (14369 bytes)  
		MIME: application/vnd.in-toto+json
