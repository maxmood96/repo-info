## `clojure:temurin-8-tools-deps-1.12.0.1479-bookworm`

```console
$ docker pull clojure@sha256:844a73a70c354267a061b93326817547abd91d32b8e363a282e02c8bd6931557
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.0.1479-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:7fb491b767495e3299edfc54159792ee251c44c60b6b0d8beb4db39845390024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.1 MB (234095556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76a0e6589947cb19583c21584c37753ff70da0f699220c11aef77e7334db6dd9`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 06 Sep 2024 16:59:26 GMT
ADD file:087f68d5558e06c7160c9322582925635e7539a7702413828357c28c77f6f345 in / 
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 16:59:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Sep 2024 16:59:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 16:59:26 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Fri, 06 Sep 2024 16:59:26 GMT
WORKDIR /tmp
# Fri, 06 Sep 2024 16:59:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:cdd62bf39133c498a16f7a7b1b6555ba43d02b2511c508fa4c0a9b1975ffe20e`  
		Last Modified: Fri, 27 Sep 2024 04:32:50 GMT  
		Size: 49.6 MB (49555051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf791cc6ffb4b486af50652d206e51b1029b1fdc187080a16968f7868e981b44`  
		Last Modified: Fri, 27 Sep 2024 06:01:13 GMT  
		Size: 103.6 MB (103611899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8172e149ec6b1da2c2214bf4becaa56a0f62422939e48e78db6df564e00dbff1`  
		Last Modified: Fri, 27 Sep 2024 06:01:13 GMT  
		Size: 80.9 MB (80927963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16bc9be9b9e9e0288d29859044375ac040ae64d80e4ff508bda1bb32b8111342`  
		Last Modified: Fri, 27 Sep 2024 06:01:11 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1479-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:9934c11c8f10772cffd44cd4b36141915ab82d33bfaa6abdf69bb4a4b64beb60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7292664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a0f740a6d0091a55a6277eb3592129077b76b17cadce4b0b04127a91681c110`

```dockerfile
```

-	Layers:
	-	`sha256:98d0428a86980b36231c2e0f890e6adf3b4103480113790ab650f35a9be85218`  
		Last Modified: Fri, 27 Sep 2024 06:01:11 GMT  
		Size: 7.3 MB (7278812 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54073f61949fe6e77dad62ce0a9b4c93edcfb6a1a9c9819701901e3347582396`  
		Last Modified: Fri, 27 Sep 2024 06:01:11 GMT  
		Size: 13.9 KB (13852 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.0.1479-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e1b94ea89dadc13e604e1dc6a71cec46b6af75d8b8328c84ee6cb6b371969cab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.1 MB (233105181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:548640bf55e01a82fd291f1b645d88770bd70928397f05c09e09884ab7a9f658`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 06 Sep 2024 16:59:26 GMT
ADD file:e689b230a6f8e5eb3500dfa6f80afd8bda70b82deda3656ddeea10df15dd54c3 in / 
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 16:59:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Sep 2024 16:59:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 16:59:26 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Fri, 06 Sep 2024 16:59:26 GMT
WORKDIR /tmp
# Fri, 06 Sep 2024 16:59:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6d11c181ebb38ef30f2681a42f02030bc6fdcfbe9d5248270ee065eb7302b500`  
		Last Modified: Fri, 27 Sep 2024 04:40:33 GMT  
		Size: 49.6 MB (49584886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64de2d331d0540719159a644987c9f3136c4aec7e34ed2283418e2bf9fb47459`  
		Last Modified: Fri, 27 Sep 2024 10:15:44 GMT  
		Size: 102.7 MB (102729247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84aa552e9086644c8995566c36dcb9caae982d10d2b1619a1c1cf643970dc41c`  
		Last Modified: Fri, 27 Sep 2024 10:19:42 GMT  
		Size: 80.8 MB (80790405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669478c05f72d0baf1fc4589fb0333c3aae961a2cf4fb874f9f60fdc788f2a19`  
		Last Modified: Fri, 27 Sep 2024 10:19:39 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1479-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:8087397c7e7eabdb0c4c50217c698b2c9271eb1ddd64eafccc214610f962fd4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7299666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84f326ab834ffdd81ac514aa73fda35ff484f847a079b78416adfa17afc570f8`

```dockerfile
```

-	Layers:
	-	`sha256:29dcaf9eeccaf21970b31ac062a94edda2f363189bcebff31ff03cceec664de1`  
		Last Modified: Fri, 27 Sep 2024 10:19:40 GMT  
		Size: 7.3 MB (7285279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c583b98fbeba6a0bbcc9f49f0af53d7c493b6ba10ab9e47fda59f4c4452c0d9`  
		Last Modified: Fri, 27 Sep 2024 10:19:39 GMT  
		Size: 14.4 KB (14387 bytes)  
		MIME: application/vnd.in-toto+json
