## `clojure:temurin-8-bullseye-slim`

```console
$ docker pull clojure@sha256:fcd40d98cf681225e8b2a8d128014110f5867154c5a5d8c44bb64c42d56bfaac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:1c22e72af114d450681840d2b0ffb5f11a1c4bc22be64cfdfa510d7f626f5efa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.5 MB (193455041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05d5e38a194a07e7906c7034fc36c1afe11856a00a634520b0faa1523e5b604c`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855293a30b8c9632aaec07f0007096f08f0b6dd5072ee7ed052a6c282e5e7768`  
		Last Modified: Wed, 29 May 2024 19:57:08 GMT  
		Size: 103.6 MB (103600211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f80d743ef8d6f6e93aeb134a6a5ced14827cea8f23e8df5b9b59e9f7d972f861`  
		Last Modified: Wed, 29 May 2024 19:57:07 GMT  
		Size: 58.4 MB (58420250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46705aa55305f5a195e51b3558200105aa38c685a79443d5644c8ed18bac5f66`  
		Last Modified: Wed, 29 May 2024 19:57:05 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f5be691ae8c6d6586cd48ad27eaf77c4eec6c4e79a8fa2187abc11f3b9d1a9b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4945591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c7b0b0190931fb6fd48734e4e3e0e1ee179df6afee188e00c050d27f8e75c15`

```dockerfile
```

-	Layers:
	-	`sha256:d05d7625eb60d7a23d000a288e1b63bb9ade7ca80acf27475bde4c202579f5c1`  
		Last Modified: Wed, 29 May 2024 19:57:05 GMT  
		Size: 4.9 MB (4931722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e410468e2750636fbfc9297e8471b457d13dc45f4fa948a5fc62afbe309bdcf`  
		Last Modified: Wed, 29 May 2024 19:57:04 GMT  
		Size: 13.9 KB (13869 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2e692ce81e7ce30ab2adcf8aabee5a2f281dd778d31e8bc60c25e34cce775652
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.3 MB (191327992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a676a80acd8ba3f6cdfcfacb05752f2f985109ce36ebba21d96ce2b9c9356c8`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
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
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96413e5e1bc47e07d164012b8a21fa2146eaf62aa0cf9162f8bba4071fc67e6`  
		Last Modified: Wed, 29 May 2024 20:27:29 GMT  
		Size: 102.7 MB (102700442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03650e60b74374ed855ac4bbb8e075d1db7d66e70ae253da95861bb4c666633c`  
		Last Modified: Wed, 29 May 2024 20:33:02 GMT  
		Size: 58.5 MB (58539995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:147bc84ea4010db4672b660c609189389e0867f3fc1be32e84dd36532881e2b1`  
		Last Modified: Wed, 29 May 2024 20:33:00 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:90227eee050729d4c5040de1be14d59c53515bcb811214835d5c18f7cd2261f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4952489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46a4fc449106e0898252e25e5cb8f0a23a040c03dcca68ef2a5ddb66fb220626`

```dockerfile
```

-	Layers:
	-	`sha256:2fa98f671b5a1717db56a9bbcb7adc9bb2cfe50fef19295ba265c83e54f11867`  
		Last Modified: Wed, 29 May 2024 20:33:00 GMT  
		Size: 4.9 MB (4938078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54577a8dc3f9add66533bffe62db59b3c06f418a83006a728a110589eb548683`  
		Last Modified: Wed, 29 May 2024 20:33:00 GMT  
		Size: 14.4 KB (14411 bytes)  
		MIME: application/vnd.in-toto+json
