## `clojure:temurin-25-bookworm`

```console
$ docker pull clojure@sha256:572ac4156c68177f3447888d20c1756ec4d32bb3749d22f23716da7b4426e782
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

### `clojure:temurin-25-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:7851a88a201a452bc36b10bc7ce24adf5159fe7118382b4b62038acd13649c8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.9 MB (221889077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5c9482352245773517764a9c55a01520937b40de0311f571445d3981552382c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 21:45:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:45:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:45:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:45:34 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:45:34 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:45:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:45:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:45:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 21:45:48 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 21:45:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cf9d22af060040e6ac300c0f415bb921c929ab0f10b74de3c85a9a925ca2c45`  
		Last Modified: Tue, 17 Feb 2026 21:46:10 GMT  
		Size: 92.3 MB (92256281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd766a2a8893b0e32682aa58feef2a8d5a783535c820b1c06a51bda17f9c81ee`  
		Last Modified: Tue, 17 Feb 2026 21:46:09 GMT  
		Size: 81.2 MB (81150269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6316f83cc303572da96e9228d7acb061070cc3c855b456a84a75aa5d8b9ab2a`  
		Last Modified: Tue, 17 Feb 2026 21:46:06 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f896119e6a276c5bead781c0dcc74164ab00345677531085edbbc63ffd6bb2b0`  
		Last Modified: Tue, 17 Feb 2026 21:46:07 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f016060bee15e498c169f7abb30c5947452a2b8c001faabb4d50077c352f1ff9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7363958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c50fc1a918fa20b1830b32a4e4165e2ef90980fa7eff16a066eea87a48e9540a`

```dockerfile
```

-	Layers:
	-	`sha256:b2739fecf98b233b3f7124a603bb5dfba830815b42b6be2e18c18b686170ec6f`  
		Last Modified: Tue, 17 Feb 2026 21:46:07 GMT  
		Size: 7.3 MB (7346187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a481bac21f6ff5b38ec5de705aba8093220acc298e9c3273be475ac911282346`  
		Last Modified: Tue, 17 Feb 2026 21:46:07 GMT  
		Size: 17.8 KB (17771 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ad37ca3485c0260de28ce21ba8359153f60bf1d6d3580a742b24b7078c6fc763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220793542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c28da20e63be3e6510cc00a20f261428bf0c6aed7c6bd54518608cb7eb7cec06`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 21:45:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:45:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:45:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:45:38 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:45:38 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:45:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:45:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:45:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 21:45:54 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 21:45:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:64e8f4c09e7ac936ecc3deb0e61613f653224c28b2e35fa9d8e6e11cbdb5f911`  
		Last Modified: Tue, 03 Feb 2026 01:13:22 GMT  
		Size: 48.4 MB (48365956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0330d742ed679dc07301b05884cd5c717ae6d9f0e827c204545474fe2a10cec`  
		Last Modified: Tue, 17 Feb 2026 21:46:16 GMT  
		Size: 91.3 MB (91288277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a151dd7bb48f5aec8eaf06c86c0f780e07d69ed4cd349477b1d71654b03f1081`  
		Last Modified: Tue, 17 Feb 2026 21:46:16 GMT  
		Size: 81.1 MB (81138264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1cb677b16d22eedb1c36503c99117d431b6e1c4084b4175a0c831f5525a4840`  
		Last Modified: Tue, 17 Feb 2026 21:46:13 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:781e6f117ef21679e2ea4924d1bf7478915f1f3759dfddec354e957000e4a25e`  
		Last Modified: Tue, 17 Feb 2026 21:46:13 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:58374040f032e1f6d2fd6b9d6842548e153703be57dc6d7e58a4dd8206706fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7369980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f9c9accb59213033a8d3092a3306c686e6c3afeca6def4a91d7424db898d902`

```dockerfile
```

-	Layers:
	-	`sha256:0ca22b13460363856af12832a6fecbde2a58c0656de27e063533bf5c9e7c6a5b`  
		Last Modified: Tue, 17 Feb 2026 21:46:13 GMT  
		Size: 7.4 MB (7352019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d8fc1158aa0c56c48c1cb513b72a1a9b8282ebd0f9f62a3f83df9e8f5d1c495`  
		Last Modified: Tue, 17 Feb 2026 21:46:13 GMT  
		Size: 18.0 KB (17961 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:d6ae605ebfa8ff4fed2d498549cb066429940de7d04761f878294ad6377e7666
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.9 MB (230948403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:013035f48441564da0716e6492aaf8eba05226dd57480f94a56ce3f641f6809f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1769990400'
# Thu, 05 Feb 2026 23:54:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:54:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:54:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:54:17 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:54:18 GMT
WORKDIR /tmp
# Fri, 06 Feb 2026 00:51:14 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Feb 2026 00:51:15 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Feb 2026 00:51:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Feb 2026 00:51:16 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Feb 2026 00:51:16 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5e189aacb842725e8d1d9877c9ab9af09e14901412b6665e179393112b5bca51`  
		Last Modified: Tue, 03 Feb 2026 01:12:57 GMT  
		Size: 52.3 MB (52327289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413bd0b8c6c326da16c676c4dc2f9ba6260e745418e4f97b3a2d3fb7fa2bf0a6`  
		Last Modified: Thu, 05 Feb 2026 23:57:00 GMT  
		Size: 91.6 MB (91632873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff49bdb92c29d1aa0a5728614463126c1cb70700342bdd4563bf11bcb84f9c5`  
		Last Modified: Fri, 06 Feb 2026 00:52:01 GMT  
		Size: 87.0 MB (86987198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7846677a8fe0a48bbcf1c1e4fdeb070ff23256f19e07d916a49d6ce8dbd9402`  
		Last Modified: Fri, 06 Feb 2026 00:51:58 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:071f8bfc37cc85641a427ac9f96190881bc3f500b3a164f6dda5b316b54df8e1`  
		Last Modified: Fri, 06 Feb 2026 00:51:58 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:66d651449302ca7e6546187bf2bf1edc83d83d991230b8c4146195df6ead2c1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7352606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6f0ed9164abe7d142a39132a6b06630c6ce4caf786ba58895f29c00284a10a1`

```dockerfile
```

-	Layers:
	-	`sha256:dd595615a846cb5160d99a3436c3b535a4f54e73ee25d800989941ce73a4a513`  
		Last Modified: Wed, 18 Feb 2026 00:05:38 GMT  
		Size: 7.3 MB (7334751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:372637b1f00263d522dd60f039aa47b548c7d138e905e41093fd6fdbb325aab6`  
		Last Modified: Wed, 18 Feb 2026 00:05:38 GMT  
		Size: 17.9 KB (17855 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:88c92c54be70a46a4acb137dddd277d53865a0b5b2a0f1a5bf80fafdef58a6b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.3 MB (215336889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5251ae2a9ae5cc3aeba6c858127cb04e823c16f3053bc012c41cac367a33674b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 22:16:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 22:16:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 22:16:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 22:16:01 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 22:16:02 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 22:18:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 22:18:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 22:18:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 22:18:33 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 22:18:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4c4c4621da5085342b3b0d8d8ef57e5e44004eedf5818268af30c41a02cb6cf2`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 47.1 MB (47138343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfba6fd0c0d82ea9631bef0d5f1a77cdb1ed5e84260880b88825e90f3037036e`  
		Last Modified: Tue, 17 Feb 2026 22:17:20 GMT  
		Size: 88.2 MB (88233833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfbc43a3c9ee33d9356cf1da6742e2ef435798f096b157c04bcb8817208f7403`  
		Last Modified: Tue, 17 Feb 2026 22:19:11 GMT  
		Size: 80.0 MB (79963673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe99df8668f427140a412788e2d3de2daeb5865f760932b0a29ada3d39fa0271`  
		Last Modified: Tue, 17 Feb 2026 22:19:08 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8601577e897e42933a2997338df395dee8210868efc3efa89e5fdc7047cd538c`  
		Last Modified: Tue, 17 Feb 2026 22:19:08 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:1bff20358a8f7fd8f6b043bbb5bc6418b6045d6d00a6cd08c4b00ddee169e34c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7339838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6742b191bb98931a989d7e4e2a59fada7bb32dca264356a927adf239fddbb41f`

```dockerfile
```

-	Layers:
	-	`sha256:dbfb8a3633211be94d5f5af2bb32df00c72b9f3491f0342909257fa53ff45528`  
		Last Modified: Tue, 17 Feb 2026 22:19:09 GMT  
		Size: 7.3 MB (7322068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13d1d226a4735dfd3956f317295c8074ef61d967ed32d0f282dcc8264ae14575`  
		Last Modified: Tue, 17 Feb 2026 22:19:09 GMT  
		Size: 17.8 KB (17770 bytes)  
		MIME: application/vnd.in-toto+json
