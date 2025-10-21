## `clojure:temurin-25-tools-deps-1.12.3.1577`

```console
$ docker pull clojure@sha256:1eafabd01e855ef05bb9f0cfa68740ccdf06ba592604514edffdb809106d00d1
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

### `clojure:temurin-25-tools-deps-1.12.3.1577` - linux; amd64

```console
$ docker pull clojure@sha256:70e5c40a7230090ff04a0526980fbd6682427d8e00952ef14fa08f18c6dcbc39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.7 MB (221665299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d304f1ecf86e2a250d128d6edd74e9bc126bfc1026c39362c7b85c541c839365`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
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
	-	`sha256:cd01849e3cbdfc6993640303768edbb56372cf9f1ae101d516334c8d462341af`  
		Last Modified: Tue, 21 Oct 2025 00:19:25 GMT  
		Size: 48.5 MB (48480563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5805c41b7595c97916ed1f1d3d2115d964f61298914d882d943bf34b91fd5941`  
		Last Modified: Tue, 21 Oct 2025 02:18:28 GMT  
		Size: 92.0 MB (92036044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1b09ba1d358b1f73eced3fd3903ec671c72b16490f17c4c77d1df231d9fdb1`  
		Last Modified: Tue, 21 Oct 2025 02:24:19 GMT  
		Size: 81.1 MB (81147653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89534c6736e552b5d1011497741503cc5d2a0ec1c80c3ce44dcb3236011ecf6c`  
		Last Modified: Tue, 21 Oct 2025 02:24:14 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3474d79177df934640d74ad65c72cd1b7f8aac6941134f05d64ac3d7fae2f60`  
		Last Modified: Tue, 21 Oct 2025 02:24:14 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.3.1577` - unknown; unknown

```console
$ docker pull clojure@sha256:3d7257198064dd6d5299ab76437ab94aa33f33a891992bb0a4dbb476e1318c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7344554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbf218e6fa80d04572facfcdaacfab36efdd0257fd0031dd881caa6a24fba048`

```dockerfile
```

-	Layers:
	-	`sha256:04ca72fdb4fe442f365c619e9956055f033a8f984c4afcc8d929224fe92ee6c6`  
		Last Modified: Tue, 21 Oct 2025 09:43:58 GMT  
		Size: 7.3 MB (7327540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74b08bd7488e0efa3fa4d8627271a74921fc283901e43fe61fc419113894481f`  
		Last Modified: Tue, 21 Oct 2025 09:43:59 GMT  
		Size: 17.0 KB (17014 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.3.1577` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4b8f14df3125cde0cbaeaa92540580f0b7750917b9aac4076bb2f31ac7f22d0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.4 MB (220433616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1a31f32a707b3e1ad02bb6c3f312dd70c2895772f3198cc1f1cd50e2ceb2e43`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
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
	-	`sha256:394d8e61f78f890cc5a49345ac4d4eb6176cdcf6b4b6af62502ae74b1662e421`  
		Last Modified: Tue, 21 Oct 2025 00:18:41 GMT  
		Size: 48.4 MB (48358996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b33ca3d6cf60049b4113fbb54195dfbe288100dcbbea36bea9717a7361325e`  
		Last Modified: Tue, 21 Oct 2025 02:24:47 GMT  
		Size: 91.0 MB (91045213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a0537702d269c954dc5b9a79f8358533f8f07e029352b94d7e3a960d8cc4a0`  
		Last Modified: Tue, 21 Oct 2025 02:29:49 GMT  
		Size: 81.0 MB (81028365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530375599816dd5c0c6ed8a123a5c30bb96d655ed56cea9a6d17ade6e6e4abd6`  
		Last Modified: Tue, 21 Oct 2025 02:29:44 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb98a63a84e0feefcdfda2de699d619972230e58aefbb71c7ec0a22eaae8de5`  
		Last Modified: Tue, 21 Oct 2025 02:29:44 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.3.1577` - unknown; unknown

```console
$ docker pull clojure@sha256:cdf217cdc35504fa19908096be6a166ca6b6af281c3593a78ea795bb54ef6f42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7350577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6b4d32470241874aa17cb3528083b68077a2f0d8281ed298074bbb8f894e209`

```dockerfile
```

-	Layers:
	-	`sha256:36d6cc6e3a9693cfc7a9eac5ff4493fdc625b8d087e26c7248d5575d03285fe7`  
		Last Modified: Tue, 21 Oct 2025 09:44:05 GMT  
		Size: 7.3 MB (7333372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8678a59a8b622e02cbcd0598b24e505142f94d0a66dbe2709fe1f90ff9a20375`  
		Last Modified: Tue, 21 Oct 2025 09:44:06 GMT  
		Size: 17.2 KB (17205 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.3.1577` - linux; ppc64le

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

### `clojure:temurin-25-tools-deps-1.12.3.1577` - unknown; unknown

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

### `clojure:temurin-25-tools-deps-1.12.3.1577` - linux; s390x

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

### `clojure:temurin-25-tools-deps-1.12.3.1577` - unknown; unknown

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
