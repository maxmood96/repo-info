## `clojure:temurin-21-tools-deps-1.12.3.1577-bookworm`

```console
$ docker pull clojure@sha256:80a7a0aec4697ca86aec84be396873224a18ec67d1b24179cdb2a371df70e2e0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.3.1577-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:4817ff67dc6c0c0e8b1ff53bbc859eb644fe963ce95a11439e3dc1ba780ad1c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.4 MB (287433273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87c677cdf7ed9fbd0c6bee091e6475bd37dea5226d11c21e69fe7c20c8471a3c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c6b11972fd12973831818babf60f1ffc1c4047507943d132dffc612884022858`  
		Last Modified: Mon, 29 Sep 2025 23:34:14 GMT  
		Size: 48.5 MB (48480557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:527d8a77f4b565fa5cb4831a065c5e31283cd6c4b0263f8807718a7ed803a915`  
		Last Modified: Thu, 02 Oct 2025 13:00:05 GMT  
		Size: 157.8 MB (157804827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6ce8bfe21a576a9d92a1a6e8395d8743b6a50cc3caec9ba5061c10a4cc40e3`  
		Last Modified: Thu, 02 Oct 2025 09:00:35 GMT  
		Size: 81.1 MB (81146848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a286eeb9416488a7e52b80977c998a463af22bceb08e2fb4060a48c33feb950d`  
		Last Modified: Thu, 02 Oct 2025 09:00:13 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dfa60564077e1e12aa5d75e545036567559d4a9d30b37dce5201d6e56de0418`  
		Last Modified: Thu, 02 Oct 2025 09:00:13 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.3.1577-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:4336eec06d37a0a885ef5207f97777f21774537bf4a93f41046eb78fe94bc22f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7395181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fae7608d9ab4b3cb46f9708ac79a4127c119ae208b5d74fff8de11eb6127dfe`

```dockerfile
```

-	Layers:
	-	`sha256:d497482a8a722eeccc052c36be5a65d4585eccd78b29294813de7aa3aca4ec4a`  
		Last Modified: Thu, 02 Oct 2025 12:40:27 GMT  
		Size: 7.4 MB (7378676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d701301cf25f37f806b6258551658fbb4e253b13b3523c55ddf92dbc2a6d3196`  
		Last Modified: Thu, 02 Oct 2025 12:40:28 GMT  
		Size: 16.5 KB (16505 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.3.1577-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b84a054484f5f45d9f682185afc168f7fdb76d1381356ec45ae8cfa7df018de3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.5 MB (285470912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8067dd710e96b86d74076738b7d1fc942bf37047156822dcb5bd93ee63475fd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f7b43f0d0a8b99591b27457b368e70a582002600d32503fd07798c1bee7cd134`  
		Last Modified: Mon, 29 Sep 2025 23:34:16 GMT  
		Size: 48.4 MB (48358915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f8ab52edafb3d3a005109deb2a5ee859fa3276aea65f33d2963a60d2a7cb94`  
		Last Modified: Thu, 02 Oct 2025 12:02:59 GMT  
		Size: 156.1 MB (156081197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7cca028c79416b9228a3181cd642595701c3bc5ded2d6ec493286109837c72c`  
		Last Modified: Thu, 02 Oct 2025 02:46:12 GMT  
		Size: 81.0 MB (81029760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b638342cd0904ca3d208de251b6e01f0016efc93bf34f0f77e207bdd7f88958`  
		Last Modified: Thu, 02 Oct 2025 02:45:55 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6841c41f6916b91f25b4e945d70f820f9f32f1012ec7cfd957dd6d6d4d5f3f7`  
		Last Modified: Thu, 02 Oct 2025 02:45:56 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.3.1577-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:be2f4c17d0787fafef51bc9b148431a07706dbee2427f206d62797629902ca02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7401110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66aeb76475c6a99fa03a669e04ea97158fb4b16625a3ad0f9f606eda121f1f78`

```dockerfile
```

-	Layers:
	-	`sha256:a46b5f16842f0fe6c19b42caf12264aa89fad0e09bac8c094a600ab86ab36eb0`  
		Last Modified: Thu, 02 Oct 2025 06:42:34 GMT  
		Size: 7.4 MB (7384463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1a1e7c3610986c69cb1019193d73a371d983cce3aec1eae94edd95424a4f380`  
		Last Modified: Thu, 02 Oct 2025 06:42:35 GMT  
		Size: 16.6 KB (16647 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.3.1577-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:98e9524f187056f330df65de70a808009776a21dae24e4b8408de3dbef2e1902
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297277233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57d9e5e52649b606ceeed6a5c84966a740c935bc4853cd9c70084a54d35dfd56`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:812b25f785969d275d8c3962568c03f83ccc4df31b95f01c0646d79d6d5069f3`  
		Last Modified: Mon, 29 Sep 2025 23:33:30 GMT  
		Size: 52.3 MB (52326764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42989fccda1d9252a9d29b9dc5277f2c0737448842a726c52eb38bbabd258df`  
		Last Modified: Thu, 02 Oct 2025 09:10:08 GMT  
		Size: 158.0 MB (157963458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dddc48125764b329d352f96161d953e014dc8ef5e4db60dbf570362ad38bab42`  
		Last Modified: Thu, 02 Oct 2025 09:21:05 GMT  
		Size: 87.0 MB (86985968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39acbdf8ae0bae7f2ff917270e664297793b286ea0ed14dade574da7a9296c6f`  
		Last Modified: Thu, 02 Oct 2025 09:20:59 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca5d8933ad56e4ce5412eb8a9dd29a128291345b27c5f035a8147d804671ea8`  
		Last Modified: Thu, 02 Oct 2025 09:20:59 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.3.1577-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:4de11ef5f4d41476e222175ceed8b3ab1b90c30b4904cc758bfb331e2c9213ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7400466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a990b23cac08882f8fb95c87d32066807793a428bc0da5dd8453184cc0eeba1`

```dockerfile
```

-	Layers:
	-	`sha256:59fd7608ce1a9f6f6c90ac7069926101221f211fff97f733a2d6d33e8a700efa`  
		Last Modified: Thu, 02 Oct 2025 12:40:38 GMT  
		Size: 7.4 MB (7383902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:856515520442bba6abcbf9cf5c212682df8431c02291784cd5776898f6e56572`  
		Last Modified: Thu, 02 Oct 2025 12:40:39 GMT  
		Size: 16.6 KB (16564 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.3.1577-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:d20516effb4670dfa623be412232583203aa515cbdb4e03fdf27b96e49cb187c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.1 MB (274122135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9fe4f97fd00c9219072e645fb272e2a9538686405d15f55e933d5d5e9e52d44`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:87d1bec83b35277b636c6e05b9418301b2f025752d7539cecae442f0b94d8fbe`  
		Last Modified: Mon, 29 Sep 2025 23:33:26 GMT  
		Size: 47.1 MB (47137446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b055c635819cb55ffe415c9020e856232341a8216466e91d8ea26d88a838cca`  
		Last Modified: Thu, 02 Oct 2025 04:42:04 GMT  
		Size: 147.0 MB (147026926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18b083c89ea156bd209c9246b44cd339415b0e3c895e822a0872491a95227a1`  
		Last Modified: Thu, 02 Oct 2025 04:48:00 GMT  
		Size: 80.0 MB (79956726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a59b3ca8e44d24125e7a0ca03c5f866127eb4c5f25eee8a77e0c022dc8beb9`  
		Last Modified: Thu, 02 Oct 2025 04:47:56 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3787d4873354cd3c67f601de8a28bd5db79afd5e51ad5051b5886e09742d9a`  
		Last Modified: Thu, 02 Oct 2025 04:47:56 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.3.1577-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:6cf0408d589a742cca2abb9689c0021f8944e6a822ba80ea084ee8b993997cbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7386500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bdc6fd32de4b9eb07c72b514286b17368365af3567c6ab2ba743b00cc2c3188`

```dockerfile
```

-	Layers:
	-	`sha256:ff0f6a0d26b7beccd3f9bbc4c0d3887585787bdc0a7f162a6ded140ccd8767e0`  
		Last Modified: Thu, 02 Oct 2025 06:42:45 GMT  
		Size: 7.4 MB (7369995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71b271f4ec24b41865a5c36bac192c262740686c6bf179a405bc721df54a2488`  
		Last Modified: Thu, 02 Oct 2025 06:42:46 GMT  
		Size: 16.5 KB (16505 bytes)  
		MIME: application/vnd.in-toto+json
