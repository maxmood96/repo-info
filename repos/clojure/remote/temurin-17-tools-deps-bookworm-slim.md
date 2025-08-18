## `clojure:temurin-17-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:82452d92a26ee05e3c53daf1914a0cd993ee5c47e685069c213ab1b3e59733eb
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

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f0405acdf2204d1dbd95e260ac529247d74b492ccf16790368e2111ee3668b37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.5 MB (242504766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:818ae50b640228321be49c516f7ea3847ac06ebb71c8625a7b5ce0f54b1246d5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e7594588946f82fe25853d3b656985a4dd1cc367b37e50c9ef26ceb919c5a2`  
		Last Modified: Mon, 18 Aug 2025 16:52:33 GMT  
		Size: 144.7 MB (144693301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13eaa5d630cf3a57602e4bac5efc9a8b2ac3988293ae2ed09edabda1bbfe1eda`  
		Last Modified: Mon, 18 Aug 2025 16:52:32 GMT  
		Size: 69.6 MB (69580168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5ebd5f8eb592f1f8239c006836685e35da265dbe2cfa82d01e006faf547e03`  
		Last Modified: Mon, 18 Aug 2025 16:52:30 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5f8b31415d549d91c2e3dc6c5f8369ef403317744e201106299af16195827c`  
		Last Modified: Mon, 18 Aug 2025 16:52:30 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0eb5785ed8dddc814d3ff8406372b99b950d24d5c969cdf7a69ff7a4a6f6bbb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5127152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2a48aa12cc9481a68663640abe465cba1adb1187d7b73fa5880c96aef0c13c8`

```dockerfile
```

-	Layers:
	-	`sha256:940b4056fdf539ba7b458e5c086c17eb397f8afa80b91147f01d46c6c35a1bf0`  
		Last Modified: Mon, 18 Aug 2025 18:37:30 GMT  
		Size: 5.1 MB (5111273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2aac8ee2ab10b0d3972c53daae047fc72eabd446d8606ee9aab9acd543e8189`  
		Last Modified: Mon, 18 Aug 2025 18:37:31 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:821160c6aacc64e0006f63e5f4a47fa5c91ffc0ab9d0ba5c822bede7f6ef00f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.1 MB (241077967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e19db995fd9e70d126a8913b253fbba385c06d972905717458af6b7086a3b48`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5cf058475776582e9e64a646c76b474fe20722c0592878e59918c738320dbf`  
		Last Modified: Mon, 18 Aug 2025 17:06:34 GMT  
		Size: 143.5 MB (143542112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfbea3217b64cebff83b69f672812035c1b5357eec2cb4ac32d0e320487bab87`  
		Last Modified: Mon, 18 Aug 2025 17:06:33 GMT  
		Size: 69.5 MB (69452809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be385477f7ecf9adf680ce240afae11cbb6da912315e3eead163cec232e850d`  
		Last Modified: Mon, 18 Aug 2025 17:09:11 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94067380cd27f3c27a25b70b53eadc53dd4dcbc28b860d6a48c3560716c389f2`  
		Last Modified: Mon, 18 Aug 2025 17:09:16 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:50c848d4e936094446ff2e081515f8b4330641c7a22f353b81a21053f7f53c6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5133031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:994316c38ffb118ed07aaf871aab8735682bab88d59729279be351c071e62dee`

```dockerfile
```

-	Layers:
	-	`sha256:a9fbf6936008363add4ef67e582017eab4ddc8bb511ff615f783945246e07686`  
		Last Modified: Mon, 18 Aug 2025 18:37:36 GMT  
		Size: 5.1 MB (5117034 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85e1197a1eba3af2bffca5985e02bb751726020e4fc5e093f7a15a3fa03974a9`  
		Last Modified: Mon, 18 Aug 2025 18:37:37 GMT  
		Size: 16.0 KB (15997 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:880d998a7df877d4a6908acf2d96ab75b88a7be8e43a54bfecab3dc63296ed08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251853547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05ed019e37cf261ae1df1e1b2241ce580ee180731a7d5fe9510f98b352c7a3f2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a0acf07605078e5950db4f22a00d81ec636270d184a86cff95e60b78f012035c`  
		Last Modified: Tue, 12 Aug 2025 23:06:40 GMT  
		Size: 32.1 MB (32073420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f775e155906486b3af9c87541a33fa50508312260cb346dd22a54dd5f4b81a2`  
		Last Modified: Mon, 18 Aug 2025 17:18:17 GMT  
		Size: 144.4 MB (144372832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b6a82b4ea2260f6ca53afa6125583fc109b50c2637a50ae6a6a1152f312565`  
		Last Modified: Mon, 18 Aug 2025 17:18:53 GMT  
		Size: 75.4 MB (75406250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316e15a84f7622d61fe917936b5e4f1d6aed0673cd04fa2b43ca1ce49ad00c99`  
		Last Modified: Mon, 18 Aug 2025 17:18:44 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5589ed420a3f6c0a1a465bfeb23a925ebcdef9e3249172636667f5c79a305f79`  
		Last Modified: Mon, 18 Aug 2025 17:18:44 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:731ce29589ac8abc1f6daf503d599f157f3cd865bec0872eba551e4301e9caa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5132358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb41399409955157ec30c3be8b6ead64688c0b036f6afddf97d4490bc93102ee`

```dockerfile
```

-	Layers:
	-	`sha256:dd04a6dd4129605a2a18bae935ee2535dcd2c4019d64ec439475d59bc555a253`  
		Last Modified: Mon, 18 Aug 2025 18:37:42 GMT  
		Size: 5.1 MB (5116431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8878d0f30c390f5f26a798494eb199748b96cfd067d5fd2d26cf8c5ff44fb39`  
		Last Modified: Mon, 18 Aug 2025 18:37:43 GMT  
		Size: 15.9 KB (15927 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:80a4ad019b695350fb972ff1e40029b3fcaabf000732c00a2c6e87e29a4afa13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.0 MB (230001352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed331b41c3f82c806ff6526a2dbe360f1783eba9f212b819b75264b9b9b35363`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5827a26ead12b66a1ef4f4d0246902cd46ee903e980906b81bf18663ea811b`  
		Last Modified: Mon, 18 Aug 2025 17:37:37 GMT  
		Size: 134.7 MB (134724369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ebb73d157492329a9e0f2b91a0d31ce6fe9c6f652ba91863951a14c75cb557`  
		Last Modified: Mon, 18 Aug 2025 17:38:05 GMT  
		Size: 68.4 MB (68388104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e7220631c9fa81f5fa07f325990e3f1ef77043713dbf085514cf9d04bebd5b6`  
		Last Modified: Mon, 18 Aug 2025 17:37:58 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:060cb72951ebec0dd1a2eb11a108e7e95d41d0b65429a48a512089e3d88cc1c4`  
		Last Modified: Mon, 18 Aug 2025 17:37:58 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:611d0a3ebeaa635033aab02e8fd16c55df939f9bea055fbe8901d95fccbc3324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5118473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:653b1beb397ea34229484e7d75feba59884a280464adfd208778f2437ad75a62`

```dockerfile
```

-	Layers:
	-	`sha256:e5940290949fd652cabdc5326ece6e8ddb1895b1368c67e85c9779fc862b0d24`  
		Last Modified: Mon, 18 Aug 2025 18:37:48 GMT  
		Size: 5.1 MB (5102594 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c31e897b60c7aa2b75a7ab249dfac175899890ae99f7b156207733c8e7b0346`  
		Last Modified: Mon, 18 Aug 2025 18:37:49 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json
