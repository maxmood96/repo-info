## `clojure:temurin-8-tools-deps-trixie`

```console
$ docker pull clojure@sha256:f134666068e1b2fd50c3e43bad7d03d791507b66f0736f35790593e185d7f6d2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:930f165d1f7be8869be9278cedbe445fb83dceca4eeb818b41775dfa4ae68f62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.6 MB (189562641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ddd5965d2b56dc412eb78aa1e42634e35b150596ef73bad24f6ff1e3666aa09`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:21:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:21:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:21:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:21:34 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:21:34 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:21:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:21:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:21:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:2ca1bfae7ba8b9e2a56c1c19a2d14036cae96bf868ca154ca88bc078eaf7c376`  
		Last Modified: Tue, 13 Jan 2026 00:42:40 GMT  
		Size: 49.3 MB (49285621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2041b7b511f0aa255db232722e6f63961c4deb13076498273832d51160cbaf70`  
		Last Modified: Tue, 13 Jan 2026 03:22:25 GMT  
		Size: 54.7 MB (54733371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8777d30fb55aa784cec7865691d33e075a8a45407b31343cfadd54b837d1eb85`  
		Last Modified: Tue, 13 Jan 2026 03:22:27 GMT  
		Size: 85.5 MB (85543006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42e1fc80dc15b8b644019f3623ccdd3a3e1f25479a38cec4f3482721638d2ab`  
		Last Modified: Tue, 13 Jan 2026 03:22:20 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e7d4048089c086386d0877d0ef2c2cf76c483f3518fdfdcebf1aa479cb8a8a24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7603604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c89e3cdf52c82c9a5aaddc3a0a38870b22336c6aab599cff4ef5d5301c2947db`

```dockerfile
```

-	Layers:
	-	`sha256:22b6bc8dab46a6d4e9a08045f36cf03dcfa7b21b318bb1496951efd2cbbac41f`  
		Last Modified: Tue, 13 Jan 2026 07:49:27 GMT  
		Size: 7.6 MB (7589434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cf19d5403cc6dae8f10858b273e52f4f75aea9b92452e3e36eb59cecd90be20`  
		Last Modified: Tue, 13 Jan 2026 07:49:28 GMT  
		Size: 14.2 KB (14170 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:791907b54be07c2686568e04d8698ce9b35e9c2f479969fd8b05b69a6032592a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.8 MB (188824716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c52587187713a61287a836519d39fa3ea21f5dcd087b5a2afa36f62f2b8907f`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:28:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:28:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:28:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:28:14 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:28:14 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:29:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:29:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:29:40 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:5582010cab7f00a8f96e076b02666116eaa7e4af9a74eb44f2946a593b50294f`  
		Last Modified: Tue, 13 Jan 2026 00:42:51 GMT  
		Size: 49.6 MB (49648083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5480ba41e3bcfb93e424f39a4c17f892847d2e9ebd790a09ce51b8ec2ece28`  
		Last Modified: Tue, 13 Jan 2026 03:28:57 GMT  
		Size: 53.8 MB (53814999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af348ed8ab01ddf84495c308cbd72abaf0ed80a23cb3b6968dfce605c9d4ee3`  
		Last Modified: Tue, 13 Jan 2026 03:30:09 GMT  
		Size: 85.4 MB (85360990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a849af8c187f2ec98eb08015cf5328377506b0a4b61359ab797e95f479f2895f`  
		Last Modified: Tue, 13 Jan 2026 03:30:03 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e7b60ccc6bf0a6c2e76a3f1a0dd602189a2dcdf2176f45d5ed15f0751b3f27ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7611450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5fc9688094937e9e3127b5e191014f1dee36edaa313952b4ab1f7b45d908d06`

```dockerfile
```

-	Layers:
	-	`sha256:d86e5366c3c53fa273039445d658ba84375be8a8f6c08e21ae74a13170e27355`  
		Last Modified: Tue, 13 Jan 2026 07:49:34 GMT  
		Size: 7.6 MB (7597162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f5078098f87185ecc5141d39cdb03498c1cf20c9e4827e58432427a1b470d73`  
		Last Modified: Tue, 13 Jan 2026 07:49:35 GMT  
		Size: 14.3 KB (14288 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:f3626535c047d88563504ec15401b3f71de99d8cff01e1a0d8d2c0c5eef76dd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.2 MB (196229266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63ae6f6f727821bc6eac46645c7b75927041147616b3816933f44208c01160e7`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 05:12:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 05:12:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 05:12:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 05:12:24 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 05:12:24 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 05:14:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 05:14:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 05:14:59 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d586c84fb9377f9b3f4030e2c3e1e9ff7b1a23a68b8abc2c48a43163a3589257`  
		Last Modified: Tue, 30 Dec 2025 01:51:01 GMT  
		Size: 53.1 MB (53108485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712597973b595c19402df1e5710d5565c7fa6467f856fa606197ec1e7e8a4aed`  
		Last Modified: Tue, 30 Dec 2025 05:14:21 GMT  
		Size: 52.2 MB (52175123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:313c085eaae9c7b40fbcd46d3a5c2f385e92c6c74552beb7fb6bca30f78b7cfe`  
		Last Modified: Tue, 30 Dec 2025 05:15:51 GMT  
		Size: 90.9 MB (90945012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70229df2fc160801a8e03d46893c4a3d1185510945eafcb65bf36da929bffe84`  
		Last Modified: Tue, 30 Dec 2025 05:15:45 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:5cb42f89b5eebc568d01fe5fd1bd3f6a60afa91bfb2612cf243e01b693b28b92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7607768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:115bf4e2c0c71e7f8d04701ef8e66402b2518d70d77dba9428bed7bbf33bb485`

```dockerfile
```

-	Layers:
	-	`sha256:49a8a20354870d819ba24e0d51972e2c58f661b075d60f164d1c8649280b408b`  
		Last Modified: Tue, 30 Dec 2025 07:40:16 GMT  
		Size: 7.6 MB (7593551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ce3698549e7c5ac091d7285e2bcb672f5cd3e3945f98f042e643f8e93e9904d`  
		Last Modified: Tue, 30 Dec 2025 07:40:17 GMT  
		Size: 14.2 KB (14217 bytes)  
		MIME: application/vnd.in-toto+json
