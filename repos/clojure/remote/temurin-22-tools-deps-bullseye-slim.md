## `clojure:temurin-22-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:4fa220555f35dbe07b8bc27de7d45c693e72a9f68f42156231e91ac4db2371a3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:68a516d66317d7294a1a8842dcbc2ed537a0578e3eb8f66ce19495ecaf06ece2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.5 MB (246535169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:508e444de10280d0131b57ca40dc877b582b5857899db67e5c082785f752aaac`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 20 Jul 2024 21:06:39 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec36eb3032d0fc48ab966398bcb29784830a89b620e50e63231f0efe66f84aa7`  
		Last Modified: Thu, 25 Jul 2024 19:05:49 GMT  
		Size: 156.5 MB (156481593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c03a5a3249d16f06b870405555bee1466f7b5d00cb92870f1d0a993ba521ca8`  
		Last Modified: Thu, 25 Jul 2024 19:05:48 GMT  
		Size: 58.6 MB (58624202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322e81228af6278df617419424ab4c28f265b75001ff18b82049ae439df9852f`  
		Last Modified: Thu, 25 Jul 2024 19:05:47 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa30c30b8ec18d004365842b6388c67f78469a0c76017fb352f3cb4dd631b362`  
		Last Modified: Thu, 25 Jul 2024 19:05:47 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:654a477d07bcd8c86ed86c13e9eb177842b3043e6378f6af2bf45a1b63ec0f89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4965333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8725442c5ddf03ed274bf90392f36e35911def7cf1a7f4e1e4c3dadd3599154c`

```dockerfile
```

-	Layers:
	-	`sha256:8bdd084c5052079641f8e40a506488063b032442cd882b9a6a3b34ac6e867fe4`  
		Last Modified: Thu, 25 Jul 2024 19:05:47 GMT  
		Size: 4.9 MB (4949820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e9615c1c8cd4bae70ddd922f626e176b1606324abde598dc7e92a26386b0da9`  
		Last Modified: Thu, 25 Jul 2024 19:05:47 GMT  
		Size: 15.5 KB (15513 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:eef68523b63aa865e5e06cf4ee85319c5cd8b19d40123f91444951a829b82f9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.3 MB (243324870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:213ba2161a64ed08f772e34ca0558f298b7273f14d0119112ee24dd3ac463ed6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jul 2024 04:18:06 GMT
ADD file:3727dfc046704936a0b983a317eeb319ebd0fc5e9da310be06a0ca768df723ec in / 
# Tue, 23 Jul 2024 04:18:07 GMT
CMD ["bash"]
# Thu, 25 Jul 2024 20:19:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jul 2024 20:19:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 25 Jul 2024 20:19:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jul 2024 20:19:09 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Thu, 25 Jul 2024 20:19:09 GMT
WORKDIR /tmp
# Thu, 25 Jul 2024 20:19:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 25 Jul 2024 20:19:09 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 25 Jul 2024 20:19:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 25 Jul 2024 20:19:09 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 25 Jul 2024 20:19:09 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:bd2a3a2ed82de858b38215fac995414b3a91eea4cfe087e5f853ec1faa989ba4`  
		Last Modified: Tue, 23 Jul 2024 04:21:02 GMT  
		Size: 30.1 MB (30076083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3578437e84830a360777bae87ddcde03bf7d0e3d58f2b9884bb3105e4bf361b2`  
		Last Modified: Thu, 25 Jul 2024 21:30:07 GMT  
		Size: 154.5 MB (154503703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34fd121e38d8cabd3a8879a3cebf96ccecf7d2b6eb71951ea6e55e7b6b3fb86a`  
		Last Modified: Thu, 25 Jul 2024 21:34:25 GMT  
		Size: 58.7 MB (58744042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7bb88d5466e4975451d9c86a4fc8bf0da99b0a745572f6adac3955228877217`  
		Last Modified: Thu, 25 Jul 2024 21:34:23 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac42f493da161cb98137ed6e6d782f4d9c19d2893926c543a2985063facf7bf0`  
		Last Modified: Thu, 25 Jul 2024 21:34:23 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:591fb2be7ea1a77a7acdf51b6f9b21af0ca2bd3fc0f767c3aee0947c021b8fd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4972230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e49b19f782556e29b10b126a61f9eb8a50047c94e3c14e4ae1149d3535820f68`

```dockerfile
```

-	Layers:
	-	`sha256:71ded69979f66eff7c38931f989c58622dc054991e177853e69b281b3607e6c9`  
		Last Modified: Thu, 25 Jul 2024 21:34:23 GMT  
		Size: 5.0 MB (4956176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9397cfb244cec97e04cd6bfa6aedc74c2a18521aae0446769600120b64ee7b3b`  
		Last Modified: Thu, 25 Jul 2024 21:34:23 GMT  
		Size: 16.1 KB (16054 bytes)  
		MIME: application/vnd.in-toto+json
