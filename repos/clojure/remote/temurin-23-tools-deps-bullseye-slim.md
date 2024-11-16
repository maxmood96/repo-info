## `clojure:temurin-23-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:ade0c43af27158ebb08e4b7cd39cf320ad83f17e6ea45bb6aad3db23cb922705
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7681c874931a00c988dcad8d683bbbb0bca6ff672eef3eeef62aef2259eb9a65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.5 MB (255487889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b97d44b4bcbe2d8086ef1ad2fad29c21fe3f05e1f2186c21e4f6780d6bdc5e6f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e209a55824a1f7a90ea5565281cfe83bf54cf39152e794fdd51f1d7f099bf1c`  
		Last Modified: Sat, 16 Nov 2024 03:51:45 GMT  
		Size: 165.3 MB (165295136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d96308e4d852c2a049047f011c8c919b92d03dd0bb4e291765a11a4c4e9e946`  
		Last Modified: Sat, 16 Nov 2024 03:51:44 GMT  
		Size: 58.7 MB (58740154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a39dd3b24f1f96be5de1ddc08f8388da0bf33c63cc077b071722393f2d6fa1`  
		Last Modified: Sat, 16 Nov 2024 03:51:43 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:706bb694f7ee5b7eb3e825bab9a54c5731b4d35e24a232c868f57cd64e12a7e9`  
		Last Modified: Sat, 16 Nov 2024 03:51:43 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e0f2bc240e779c2c165dc65b3b716b63464c5c1d3c200b877c860d5b934cb69e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5146243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ecd10e3f7deae5511d2ca6c70517fb276949e6d4eb479b0510491054b8100a3`

```dockerfile
```

-	Layers:
	-	`sha256:ba5139f10e21c3415e0a16a862c6ad596449d0514acd4d2abfd30fb9c71cd7ee`  
		Last Modified: Sat, 16 Nov 2024 03:51:43 GMT  
		Size: 5.1 MB (5130365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3f5d67df7feefb308d7465a0752e6d0bb444094ca7767faf0ea776246cdb22a`  
		Last Modified: Sat, 16 Nov 2024 03:51:43 GMT  
		Size: 15.9 KB (15878 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9414d22b921e2d699ffc38fbc4929648f56ed227189a402a6cc4aee2195ac855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.2 MB (252249874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f7eb40482381a4b3bfe7b34acd0c3120d11b0c298463186b804bd3d20b41ce4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28ca6f73ecea9eadb356f63023098f39244b4749ad15cf045cbfe2b62999eaa`  
		Last Modified: Sat, 16 Nov 2024 05:49:47 GMT  
		Size: 163.3 MB (163281799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1debda06ee56a62d2f6683f9df7e4e52014f7c25bf4edd62d7d93dd83ce3fd9c`  
		Last Modified: Sat, 16 Nov 2024 05:54:10 GMT  
		Size: 58.9 MB (58875436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ccad201912530f864ac805a0816a397f8402394cea25e3d4c1d31ff2cc6b08`  
		Last Modified: Sat, 16 Nov 2024 05:54:07 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2818993103b1dfe6d1bac7a56dc614db614f05d21f6219958c5463030adef5`  
		Last Modified: Sat, 16 Nov 2024 05:54:07 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6ace5eae4a9be1572179cccf0ea83dcf6d3db8591962275e66ff5dc2caed913a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5151474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf563d003db3015a1db32716c344b78e35ca83e1ce13ff413e0d6061b6baac66`

```dockerfile
```

-	Layers:
	-	`sha256:16185335a4a2562232c77f9715ad24affc636cc7be415b7e8a0f6395823d6ce5`  
		Last Modified: Sat, 16 Nov 2024 05:54:07 GMT  
		Size: 5.1 MB (5135480 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92a5939ae76bcdfa3810779697e1f9b43df97bdd7e871d7664ef5bc2c2fdfde5`  
		Last Modified: Sat, 16 Nov 2024 05:54:07 GMT  
		Size: 16.0 KB (15994 bytes)  
		MIME: application/vnd.in-toto+json
