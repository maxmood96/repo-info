## `clojure:temurin-11-bookworm-slim`

```console
$ docker pull clojure@sha256:3003a200865fb3c21e356c3be07ddb8761e4d97c601374573d1c5429453f88eb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:6df5c61146c858c1646b90a52cb4b1774312b8de55a38e206f9a075d15121b37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.7 MB (243699182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f640d9be303d72ddb5fd6661f3f5f600770d54ae4aa93f7e4bd2752f1efdd925`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 20 Jul 2024 21:06:39 GMT
ADD file:6c4730e7b12278bc7eb83b3b9d659437c92c42fc7ee70922ae8c4bebfb56a602 in / 
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["bash"]
# Sat, 20 Jul 2024 21:06:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 20 Jul 2024 21:06:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 20 Jul 2024 21:06:39 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Sat, 20 Jul 2024 21:06:39 GMT
WORKDIR /tmp
# Sat, 20 Jul 2024 21:06:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:efc2b5ad9eec05befa54239d53feeae3569ccbef689aa5e5dbfc25da6c4df559`  
		Last Modified: Tue, 23 Jul 2024 05:27:55 GMT  
		Size: 29.1 MB (29126287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aed2ebf64e06b05c1d926c204b8c539e1180d29413b13dc837d515d0402eaf4`  
		Last Modified: Tue, 23 Jul 2024 07:14:02 GMT  
		Size: 145.5 MB (145504812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0fff66d8fe213011586117ee9b97accde3ad705063d0e92adad8c087829e86`  
		Last Modified: Tue, 23 Jul 2024 07:14:01 GMT  
		Size: 69.1 MB (69067438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb47157a11123ec610b516777811e62624d9a78e3df1ddb00157ad5a1d5bdad4`  
		Last Modified: Tue, 23 Jul 2024 07:13:59 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4572b8680ab25815582b76899c4b460f4443c741046302734589bd27edf14c63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4759100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f871f1ea9c013fddfd2c554fd0ecb4561098e28d9ef13ed26988e9d3e262db0c`

```dockerfile
```

-	Layers:
	-	`sha256:632f6e4aaa598f6daa73be8f0ed345719d58dcce553eccd0d0d3b0ae389c4f4f`  
		Last Modified: Tue, 23 Jul 2024 07:13:59 GMT  
		Size: 4.7 MB (4745164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88718b59a5c5eb227765f63433829050f4123e33202348fce4e08b2b5b8e1776`  
		Last Modified: Tue, 23 Jul 2024 07:13:58 GMT  
		Size: 13.9 KB (13936 bytes)  
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
