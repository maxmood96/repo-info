## `clojure:temurin-11-bookworm-slim`

```console
$ docker pull clojure@sha256:3b66374a712cabdc48fe6bcdb582a9dcd2c5caa184df7b5cc5cec0ed82180436
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e3fba5f60cbeb63aa191ec09a12d246eeddaff6aac24e83deaa27189c05c7449
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.7 MB (243698273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2a9d3331a5edea3e4347573e1c2c962ee3e129fd66e5a5b18fdcd99c0e337c9`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
# Tue, 28 May 2024 15:17:11 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a903a3774a7db8a9944f47cc4df219693f1e6a2c6989c369b9e1cb5091445e39`  
		Last Modified: Tue, 02 Jul 2024 07:07:01 GMT  
		Size: 145.5 MB (145504824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1dff225357acee71de46a1812a65a771fbe3ef52a465f87295ae140945a8493`  
		Last Modified: Tue, 02 Jul 2024 07:07:00 GMT  
		Size: 69.1 MB (69066528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2ca61141bf3973288ef56e4dbae761e7f524d2226b6fd3064b205eba340aa0`  
		Last Modified: Tue, 02 Jul 2024 07:06:59 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2ffac4fc1dcb7a9d702af31169d5bb472a61ca4c348a705f1ae89215123f98c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4718976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6654e7b487cdfffcd70cf0991da65b93fa54e4bdf4b26c999802a0d4bf034e9`

```dockerfile
```

-	Layers:
	-	`sha256:e244b6f863ed56a5c0e3cf00fbfbd9e9792df66c1afd02f4879fbde9c11d3c5d`  
		Last Modified: Tue, 02 Jul 2024 07:06:59 GMT  
		Size: 4.7 MB (4705039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92885d32c63bb0c26a65369a56325c14b2f59d00ba3ac20051abfb2be7e439c0`  
		Last Modified: Tue, 02 Jul 2024 07:06:59 GMT  
		Size: 13.9 KB (13937 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9c22134d21db80557e61f81fee43bb9c481b5c6087b12c3fd7c98ddc75a47b2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.3 MB (240279925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:125b2be6353b5e2de5bd1bfc1cb9d46e33329c0bc8a9d87e7b0c8b9b1fcb025e`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
# Tue, 28 May 2024 15:17:11 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd4487946e60f180297b8ae2f413caa86218e4556e23d06a047f6563e9db3fa`  
		Last Modified: Tue, 02 Jul 2024 09:20:09 GMT  
		Size: 142.3 MB (142304047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4161c1cb4bd1e6d2a61e09060c5e3f6fcbcc013b19d3ccbc704cca0e3aba8054`  
		Last Modified: Tue, 02 Jul 2024 09:24:04 GMT  
		Size: 68.8 MB (68818672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1bfa723fc2e22e82fcd1050ba0ff125b2f70a842f00c0fcb410a59aea1e335`  
		Last Modified: Tue, 02 Jul 2024 09:24:01 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:153104caf08604ac3665d7f4fe5f82e0deddddd5c4fe0ba0a775fb7490fea52b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4725902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ce7a3e143151b6acdba25ae4c2a9cda724d669674d5371ed4d64d4216c2e0c`

```dockerfile
```

-	Layers:
	-	`sha256:3f413bcb5d1270e66aaeadf5286d962a172c4612e227696b8f4c57ffc0c7d8f6`  
		Last Modified: Tue, 02 Jul 2024 09:24:02 GMT  
		Size: 4.7 MB (4711424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48562865cf5f6f15683ade0a88aaa94ec3b785aa198f104c95540a66507be756`  
		Last Modified: Tue, 02 Jul 2024 09:24:01 GMT  
		Size: 14.5 KB (14478 bytes)  
		MIME: application/vnd.in-toto+json
