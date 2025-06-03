## `clojure:temurin-11-bullseye-slim`

```console
$ docker pull clojure@sha256:c5243783e4b580c6dfdf17d48c0591d8ad8c0f790e837b48dc1000608ec79245
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:bd7cdb04af0fba516f9ecab806b2b666ce589ecba46f92705844bf7c2fdb55a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 MB (234897997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec4c9faf2d842effbc7c6c40d0870181b254b0a01b049664147c27558682fea0`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:e1f16b66c2e86ad38458eba597e4ec79e4750398a28dbbc2d7819d829c4c9023`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 30.3 MB (30255940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c4887a813ed0b9ae7bb7afca945323e628e7133e781964b54cb4992a722b3b`  
		Last Modified: Tue, 03 Jun 2025 18:23:58 GMT  
		Size: 145.6 MB (145635655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:286c48b2591fb52c06aa6d19cd4136ac69407563162a04941ae418f14d7f6a80`  
		Last Modified: Tue, 03 Jun 2025 18:23:57 GMT  
		Size: 59.0 MB (59005758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4549815dd8ceb312d241099ed59cb316e740bb45b243361a06d1d1c1979d0cc`  
		Last Modified: Tue, 03 Jun 2025 18:23:56 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:076b6e2e3f46e81484960819b3d08dd0dea75795a7d6625017d39c2235db6326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5203036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:197ab795afd89520712a5877be6cf73a5a5fd8f4cad8fa475664a5c6ed75abf1`

```dockerfile
```

-	Layers:
	-	`sha256:fbb2f4a28acef6c7d8f2c9518de28e16243038ac758728b269d80d44b1e0c349`  
		Last Modified: Tue, 03 Jun 2025 21:35:22 GMT  
		Size: 5.2 MB (5188727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63a58585678bbc31f6e5e54d9f939b26b45a9e160ff4a7a72c6fc7d7a96745c3`  
		Last Modified: Tue, 03 Jun 2025 21:35:23 GMT  
		Size: 14.3 KB (14309 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0f30b1e1d9facb03ca7e3d79797a1f31b70c93aef9f4edd34a7e0f3937abdd7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.3 MB (230305148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8ecde83984cbc107a7d58dcb51bd08618ac16ae73841afcb976131716f19350`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:66850c8b65c1e9c3674a722b71f8887dd317a9b257148bb1063e88d85790544f`  
		Last Modified: Tue, 03 Jun 2025 13:30:45 GMT  
		Size: 28.7 MB (28746257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:192c7e75dcf364b2ceee07e82338697627a9716867e83933b2f790e9d0962da2`  
		Last Modified: Tue, 03 Jun 2025 13:34:30 GMT  
		Size: 142.4 MB (142420666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6302bec43dcadcc8a5c222cb53140543cc5ab69ce691f5b8bc9291fd357a6a7`  
		Last Modified: Tue, 03 Jun 2025 18:34:58 GMT  
		Size: 59.1 MB (59137582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa318ad5f6c9edd6e5a2c279f8affb3bc05ad1f4ca024cbb47b5e5f01577531a`  
		Last Modified: Tue, 03 Jun 2025 18:34:52 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c48a0201c717b1af65cb8dede9b6c6a9f5b17d2d674e515e037c91b1edb5cf88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5209505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e8224dffaf6f2bfbd6219a044b416b5553e041be1b792b59b5f1f066e0d9311`

```dockerfile
```

-	Layers:
	-	`sha256:1462a0cb5243b6835449bd027196c849d1e8c8b31e49590968a329f9b8e705fd`  
		Last Modified: Tue, 03 Jun 2025 21:35:29 GMT  
		Size: 5.2 MB (5195077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c2b32f10d131b41d9a1f8e3abd8b05f50f7e759816177943c85ee868ffaa997`  
		Last Modified: Tue, 03 Jun 2025 21:35:30 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json
