## `clojure:temurin-11-bullseye-slim`

```console
$ docker pull clojure@sha256:90b0ce32670266777543146296a7e6203e6a48ea77dd7ff88c322f5390abaa8c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:1094069f22042cc1a04521752c76b68f20764c5e7706f4896b427d56fe1c2d92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.3 MB (235331414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03e44005806606dea427e234c5e19544ea9d2aec4726ab859cb273ab258c7486`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 19:43:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 19:43:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 19:43:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 19:43:57 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:16:18 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:16:31 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:16:31 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:16:31 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:77e30ef52aeb52d8466baf0f50b54ed2fc0b421f44c49e5bf93682b27110f4d3`  
		Last Modified: Fri, 08 May 2026 18:22:59 GMT  
		Size: 30.3 MB (30257958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4988322c4b96a6b2ab6e52a9f7dd92de2757730c6fa104a47ad69b1e1bf7ef`  
		Last Modified: Fri, 08 May 2026 19:44:39 GMT  
		Size: 145.9 MB (145886217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a5f19101cd491a0e788cb1c2f00918d26aa9d6877d62f15169ae863f6f9eda`  
		Last Modified: Fri, 08 May 2026 20:16:46 GMT  
		Size: 59.2 MB (59186593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5fbdf0e32b0b318b6972bfba331a01dfad2b7b543d25ebc4ec70f0468372e06`  
		Last Modified: Fri, 08 May 2026 20:16:44 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6dfd9740ddd709e5fa61a412e64d98c52cdae4c1f1a69e6e862e6a0d3f9754e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5354614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a71562d113f86f16a3e368aed1b8bdb29c817c4689a90373cbcfefcc72fa71e1`

```dockerfile
```

-	Layers:
	-	`sha256:47b87300a3426e91519337b990184b80b4241e9484c704c2b58f24b4a3596819`  
		Last Modified: Fri, 08 May 2026 20:16:44 GMT  
		Size: 5.3 MB (5340196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1e0fdacb79068531373dc9f795b6af8bafaaa1a59930e3e9da0bc85b24d059b`  
		Last Modified: Fri, 08 May 2026 20:16:44 GMT  
		Size: 14.4 KB (14418 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:86476ee97f304f43e6a52fa33bf8131c2d2f0516f75f561beabe28cc96f4b8ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.7 MB (230656648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f3b7109c251a083459e1b1d87268ef787caa8980e82ff4587c41acf41f19686`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 20:20:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:20:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:20:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:20:23 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:20:23 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:20:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:20:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:20:38 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ab0f13d792ff9100407906fb422a0b62a8b437abde4c245e03f0366814be9aae`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 28.7 MB (28742591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eaa0d6cf30054d11ef7017bf37e0d9a554ee1fedf58adf11ce256463a3618ad`  
		Last Modified: Fri, 08 May 2026 20:20:59 GMT  
		Size: 142.6 MB (142582223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5178d28f4ba521732b1cf507c0b72cf281f50085e3f609b63fe3089af6a35979`  
		Last Modified: Fri, 08 May 2026 20:20:57 GMT  
		Size: 59.3 MB (59331187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7afc87246a2b9dbd9bec94bfdd1ae0e178b8bede43a90c6f9932e84d2d54b47c`  
		Last Modified: Fri, 08 May 2026 20:20:55 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c498132a8057ef19354e79003ef9ddc011d3cf5fa9da7c9e96a78b2165b16927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5361085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80913c08b7934ce2ea3d5e0627c9581516bb80d7238aae7dd8a6df4ba933d3b3`

```dockerfile
```

-	Layers:
	-	`sha256:e41b036efae8e1dab565a702114f7addc33d74166045821c252b46e692fc98ac`  
		Last Modified: Fri, 08 May 2026 20:20:55 GMT  
		Size: 5.3 MB (5346546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:752220df711680a21b538b872e34598283738083384fcdf792c9494617a1ac90`  
		Last Modified: Fri, 08 May 2026 20:20:55 GMT  
		Size: 14.5 KB (14539 bytes)  
		MIME: application/vnd.in-toto+json
