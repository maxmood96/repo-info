## `clojure:temurin-25-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:855e3a25d97d65bf5b1b1baff4d79dcdfa79a2e59d3727954344d3a1655b86e3
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

### `clojure:temurin-25-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:2439c28f3e93f6887040cf93188527b4797aaa1a3fdd68264df17798a36ea301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.7 MB (221664550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b65af19b5d694955c39833b1cce5cd08af00b833cb442e1da48432693f8ee3f`
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
	-	`sha256:cf20ac60ac4c1bfe7ba8f5839633de89d13b7866956e513e423fce135432fd5b`  
		Last Modified: Thu, 09 Oct 2025 22:26:21 GMT  
		Size: 92.0 MB (92036049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91a464ddb73554021ab185e5c58511627f11a021bdd73e8524ce473d5c3dcc20`  
		Last Modified: Fri, 10 Oct 2025 03:44:45 GMT  
		Size: 81.1 MB (81146902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55963c6300862ed48c5ab6a115fb6df3a5136c60baa5d81c4f7006555cce47ec`  
		Last Modified: Thu, 09 Oct 2025 23:14:46 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a84c46a9c3261a19d39ed479822edf805d442b2df916a86c2f27333d9d845e7e`  
		Last Modified: Thu, 09 Oct 2025 23:14:47 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:a6c757a0aa3fe7feb7948a065f13bae2b9a89ed9236d582dd09a9fcc830850c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7344555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bc4206fecf5ef4a0f26f5de6842c7f79db200dad4a923a314d672a960327fa9`

```dockerfile
```

-	Layers:
	-	`sha256:a33365b91abaf89708f02dd3b84a06968d163504be8fc2b766172ff7a939e7ac`  
		Last Modified: Fri, 10 Oct 2025 06:47:07 GMT  
		Size: 7.3 MB (7327540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffc737ec49beb8c85f8839064227920e2682e244b800f80d726e72aee9ab239b`  
		Last Modified: Fri, 10 Oct 2025 06:47:08 GMT  
		Size: 17.0 KB (17015 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6352e941714d9f124e9394999123aa9726ba68723ab6d0ad8b09fc45f75d91c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.4 MB (220434640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34e75c990b4948cf4d901307728ea76cced47535e276dc4d07a8f425877063cf`
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
	-	`sha256:e564b38894736b0fcc9216857ad6cfbcb2ee1f45d934cdc44e9948ddab5131aa`  
		Last Modified: Thu, 09 Oct 2025 22:31:10 GMT  
		Size: 91.0 MB (91045227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a0e9fdbacb2f79eb4a8eeda538cc3cc3a0daa39943bf480022eff6c77a8469`  
		Last Modified: Thu, 09 Oct 2025 22:31:09 GMT  
		Size: 81.0 MB (81029456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee072842e951a5f4d6baa1aff1dd7e9ef8c0d5c94bfcc84c1761b68e169f5255`  
		Last Modified: Thu, 09 Oct 2025 22:31:02 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbaa9ce42205580c3045b204fad2d029839be375e85b0c817d336c7aa2154551`  
		Last Modified: Thu, 09 Oct 2025 22:31:02 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b9412c59bc6565430304a1ee07a54e7691cc4295eb90f5821a662fd0cbe38bd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7351376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f30de465e34b8c47cb81e56e01ad303280cb339a0676a476c5d37b7373804ed8`

```dockerfile
```

-	Layers:
	-	`sha256:dc77e05b193d16ece2532d2fb6a4369236d105dff40040c3d90b050d25d9be9e`  
		Last Modified: Fri, 10 Oct 2025 03:38:29 GMT  
		Size: 7.3 MB (7333372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9175e0d78bdfc60f5fb81fd692d4cf7b82b1b60920777bda9056cbd4483bc206`  
		Last Modified: Fri, 10 Oct 2025 03:38:30 GMT  
		Size: 18.0 KB (18004 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:75e2244bd7a12da766eb285bf4812407cbdec3ae307715a991f8fd8ab38c1419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.9 MB (230914932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ae3f33c70fd9c29780ba659c73cc401c676843d84bb2cfb1d3dbbe9473747d4`
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
	-	`sha256:9a0781477181b5af5ec1c569a15deaf01c73878e068638e740e70d8e99fef2b4`  
		Last Modified: Fri, 10 Oct 2025 04:40:19 GMT  
		Size: 91.6 MB (91601717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:761cd834751df86d37ab31a981f46e386d0fcb060a67cd76c6ba8e10b893ac4c`  
		Last Modified: Fri, 10 Oct 2025 05:59:05 GMT  
		Size: 87.0 MB (86985407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4767ab62f530382c79463878b11496bf070289ed9b6bad5937d988a143aeff40`  
		Last Modified: Fri, 10 Oct 2025 05:59:00 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f74ce319dbe5e14738aa0950ac91dc1f8203b9b0482f7ef86af55cbdcb3e27e`  
		Last Modified: Fri, 10 Oct 2025 05:59:00 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:7b669940ccd6dc25e643364e8a82d0b890d2ca889beeff7cc2954a5b0ac53e74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7351985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cb71e0b76f077c7df4ff50b08bb4bb322b09d874d2433395d020d2726e2e9ab`

```dockerfile
```

-	Layers:
	-	`sha256:a0212b9ab9698e547a428f4e21cc1f474ada54c9f6dca2439d36d28c6ca9a9d4`  
		Last Modified: Fri, 10 Oct 2025 06:47:18 GMT  
		Size: 7.3 MB (7334088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bba820122dea01b08afa90da5606a2ee8b07cca4eca3e5103c466566b44b334`  
		Last Modified: Fri, 10 Oct 2025 06:47:19 GMT  
		Size: 17.9 KB (17897 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:7cdea8ce5e0fb71158d3e82d1e3b334a885c0926973af26ed703f8c1235c0a30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.3 MB (215301482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23be078a1b328a558ad40cb44065f915191d061d0b33dc1de536f73c8e582810`
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
	-	`sha256:d0377f9dba375d95cb49de92a8238c46c38f8e06ec3ab5ee54df5d9cfa7d596c`  
		Last Modified: Thu, 09 Oct 2025 22:50:23 GMT  
		Size: 88.2 MB (88206454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1fb9b24eb065263bfd38a77e2470fa119fe8a09b6f0b9c9beddb6ec4dac202`  
		Last Modified: Thu, 09 Oct 2025 23:48:14 GMT  
		Size: 80.0 MB (79956540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b358ed68a3b042151841e6cbac166dbfeeaa8deb52027ef1272eac0694edaad8`  
		Last Modified: Thu, 09 Oct 2025 23:48:10 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac325d0149e2edadb82ff50baede78095e93c062db945bf7ac6c21ef351753f`  
		Last Modified: Thu, 09 Oct 2025 23:48:10 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:1a6ed07403cc8793efcabc05221bfec140f55206d57c7381f8912f65d94dc36e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7339221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce4ba977d5c9a8cec195525b61c7080a534508e81fb28511b811c8ba94ec9510`

```dockerfile
```

-	Layers:
	-	`sha256:b942cb2afde237e834f8b26760a600eaa19f65f267ba9b03bf22d070d4a0c9b1`  
		Last Modified: Fri, 10 Oct 2025 03:38:43 GMT  
		Size: 7.3 MB (7321407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:338cbd53899ef9f68230e32d6c084e667e22d81e5c15d43a66083f602dfe437e`  
		Last Modified: Fri, 10 Oct 2025 03:38:44 GMT  
		Size: 17.8 KB (17814 bytes)  
		MIME: application/vnd.in-toto+json
