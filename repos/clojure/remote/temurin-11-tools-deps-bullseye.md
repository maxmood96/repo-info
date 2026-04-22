## `clojure:temurin-11-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:9f77215460e0a53bf949cd5bdd031db323695df607a6383fa333b4382c9bb5be
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:819fd813d576e3dd5c40dc267daac9a7a9109cfdb5469922ca7b0cb64fea5a62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.2 MB (269171097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43631693e79437eb1fc8647059da6749af0dec2ed30f43b390623cc842fad8eb`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Wed, 15 Apr 2026 22:03:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:03:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:03:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:03:03 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:03:03 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:03:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:03:17 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:03:17 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ced3088fc7691915325d6187786ba346149f7c9dcdbfb3772ca71be74bf87622`  
		Last Modified: Tue, 07 Apr 2026 00:10:43 GMT  
		Size: 53.8 MB (53762793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694a66ecbc5c5c6013c126f5d3310ca21ddab21b654c846199da52cca5a562dc`  
		Last Modified: Wed, 15 Apr 2026 22:03:42 GMT  
		Size: 145.8 MB (145806800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c725499eb0cfc8944024b0313faebcddc6413f0ca865a97fe499d2d74ce6cd75`  
		Last Modified: Wed, 15 Apr 2026 22:03:39 GMT  
		Size: 69.6 MB (69600858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56e96027c648326f4aab65c567373ec9ca4425f3e547f1b5b7482090b58bfead`  
		Last Modified: Wed, 15 Apr 2026 22:03:36 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:cc407f23460363af32df44553189934d8b3701d05f1f7eca8c4f69a952b44b0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7442003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c711b634093e4fa631c8196b43ea23185421c530ea532e3e4dbedaead3ff9ce6`

```dockerfile
```

-	Layers:
	-	`sha256:eb56fa26e2079466b964f044debd8635bf765d9c22ee42055fe89c580f297baa`  
		Last Modified: Wed, 15 Apr 2026 22:03:36 GMT  
		Size: 7.4 MB (7427794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8eeb904fce4f574f3b89956889abf2e9096d6ad7def16a225b63f044754c4818`  
		Last Modified: Wed, 15 Apr 2026 22:03:36 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:66519e9330e92ffb7138edb76728a99a64d65f725ef46d9e847c7db80b99992a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.5 MB (264493114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ef5734ebcda898a64d8db5edb68c161d781fc26a0a8b0f9d64dca50acb1165`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 02:21:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:21:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:21:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:21:02 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:21:02 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:21:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:21:16 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:21:16 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d66293db501a72163d605baf6b3e8451c38d0fe30b934c24cec53a4e66b6e46d`  
		Last Modified: Wed, 22 Apr 2026 00:16:07 GMT  
		Size: 52.3 MB (52253001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8264133c78629ca956d7a8adb4df8a3b76ad66f18b58c3a1136dcc467e37377`  
		Last Modified: Wed, 22 Apr 2026 02:21:40 GMT  
		Size: 142.5 MB (142500803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae1be4c5afda5ed48809d771485d30b30d5e6e6d7fe7ad800ec0fc54421ac97`  
		Last Modified: Wed, 22 Apr 2026 02:21:38 GMT  
		Size: 69.7 MB (69738666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46fe150de87c5636be407a82aa9958b78150c0fe715dde0e94be9891d9ef797`  
		Last Modified: Wed, 22 Apr 2026 02:21:35 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:127d1486ca5fc2ad1869ef365a33e2de3ab419be8b4b48264d39a7365d1f6120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7447838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7e27e2dd529eddc19182f766d13008817adfbf05f2122b407f9530115a026fc`

```dockerfile
```

-	Layers:
	-	`sha256:9d92ff28e04fccd7276db9e029e1511fe2642b280eb9e99a93097bc8bb13d6e5`  
		Last Modified: Wed, 22 Apr 2026 02:21:36 GMT  
		Size: 7.4 MB (7433511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:469bfd6e78be145b1d72932b802a3e03a754164b4a31c09c47871aa567c09f67`  
		Last Modified: Wed, 22 Apr 2026 02:21:35 GMT  
		Size: 14.3 KB (14327 bytes)  
		MIME: application/vnd.in-toto+json
