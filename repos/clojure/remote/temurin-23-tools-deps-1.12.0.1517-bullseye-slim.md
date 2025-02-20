## `clojure:temurin-23-tools-deps-1.12.0.1517-bullseye-slim`

```console
$ docker pull clojure@sha256:70da1cda236e6893ea510123dfc5eec3c3c4b9f4aff1f084158bba59e17dd0a1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-1.12.0.1517-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:25056fa388378b85aabed27c01e3f8037ed4b8723a85407e9a2b65fdc05c572f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.4 MB (254358205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60a29b1043b6d34b6d4c037456ad3dcf81fa456e464b0c903daaa9822a4224c8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Wed, 19 Feb 2025 14:51:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 19 Feb 2025 14:51:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Feb 2025 14:51:07 GMT
ENV CLOJURE_VERSION=1.12.0.1517
# Wed, 19 Feb 2025 14:51:07 GMT
WORKDIR /tmp
# Wed, 19 Feb 2025 14:51:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ba7f99d45e8620bef418119daca958cdce38933ec1b5e0f239987c1bc86c9376 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 19 Feb 2025 14:51:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 04:26:31 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b18063e0754e80b1f5340589692924835df9b05a522a886ff827f88183e83d3`  
		Last Modified: Thu, 20 Feb 2025 02:31:33 GMT  
		Size: 165.3 MB (165316204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd611aa3c95198ddb2f620dcd3933642573b248238e1205a50a7f7353d5604c`  
		Last Modified: Thu, 20 Feb 2025 02:31:31 GMT  
		Size: 58.8 MB (58788374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a219d3a7f52e802a57f3f3d33444d575948fbcc7a86d041a5754981e741b6e`  
		Last Modified: Thu, 20 Feb 2025 02:31:30 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b1beeb6e8bc4c5592b20ba4fcf8e2d2af1e922f80b3eef71807560bdf0a0e68`  
		Last Modified: Thu, 20 Feb 2025 02:31:31 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1517-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b2245adec38f93e80ec03dcf4cfb18128d41b822d0f1677f643ffebef30ca3e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccedef81ee38f2a9048c41ed14b8cf68a3a0e8805896d3638469d5d9034dc109`

```dockerfile
```

-	Layers:
	-	`sha256:76b22b19b31b4f1a9045b2baa9162f94d99c8ced8429959ac73311c00af2deb4`  
		Last Modified: Thu, 20 Feb 2025 04:38:04 GMT  
		Size: 5.1 MB (5122072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ebee5ef9b2f5e35b72e5fba5c8172780508763d58ef80ab3b74bbfd5c9890fa`  
		Last Modified: Thu, 20 Feb 2025 04:38:05 GMT  
		Size: 15.9 KB (15878 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps-1.12.0.1517-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4bf87aeb4f708edfabd1062a1bb7f1770e4bb81fff7a1f6100cf41844a30d5aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.0 MB (250997716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b9ad5b6f2226f8fc73a0fe90f4a25b9c14cf2fb4d675418812dad25daf49d04`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1738540800'
# Wed, 19 Feb 2025 14:51:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 19 Feb 2025 14:51:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Feb 2025 14:51:07 GMT
ENV CLOJURE_VERSION=1.12.0.1517
# Wed, 19 Feb 2025 14:51:07 GMT
WORKDIR /tmp
# Wed, 19 Feb 2025 14:51:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ba7f99d45e8620bef418119daca958cdce38933ec1b5e0f239987c1bc86c9376 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 19 Feb 2025 14:51:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9225a2a808e874449ee822a282882a3c331aad2f5093c1062e16494d8bce3e9a`  
		Last Modified: Tue, 04 Feb 2025 04:27:50 GMT  
		Size: 28.7 MB (28744810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99325087be61afbd535597066d8cb53ded2733e364a918534e5aba3076419709`  
		Last Modified: Fri, 07 Feb 2025 06:58:43 GMT  
		Size: 163.3 MB (163341440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d248c429955dde03c9673baf09722e7d203311785406f9c29137af5fd1b458`  
		Last Modified: Thu, 20 Feb 2025 04:04:35 GMT  
		Size: 58.9 MB (58910424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a8e3f9a256f93c79fe30784a6fb6948e24bbf4db380d40edf6440af922b2aeb`  
		Last Modified: Thu, 20 Feb 2025 04:04:16 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91275d72e22cb67e3e88489855dd620429ebc0382c48816ef90c05b686662b04`  
		Last Modified: Thu, 20 Feb 2025 04:04:18 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1517-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0e8496f2913a249952beaac80b7bdc22daca1f65dae7d7e7b84ae4cc25df0488
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5143179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2170683860c5560f0ce5942751c5ef3c63d358e4f2c9ee82991f5168a06c117`

```dockerfile
```

-	Layers:
	-	`sha256:7756330acc12d3f6ac347cd4cea079e59a4a50b5266fefd7ba0f04524bde3790`  
		Last Modified: Thu, 20 Feb 2025 04:38:08 GMT  
		Size: 5.1 MB (5127183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3d6cc30fbf0fc159adad4a710582c91b0570cc69fd7354b82ab84eddb2c33be`  
		Last Modified: Thu, 20 Feb 2025 04:38:08 GMT  
		Size: 16.0 KB (15996 bytes)  
		MIME: application/vnd.in-toto+json
