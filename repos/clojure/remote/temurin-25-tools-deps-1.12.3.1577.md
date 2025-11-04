## `clojure:temurin-25-tools-deps-1.12.3.1577`

```console
$ docker pull clojure@sha256:1772255d15ed3f049351b1b0dfea166f82deaf6356f2a49a1345d2d785532848
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
$ docker pull clojure@sha256:f4dc251fc33b2e9ac4343e40766781a8e263186a417e92b62dfb5585b1edd78a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.7 MB (221665340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2116d14dc8cceadaa654598aadeb37e8d674e0b7bbdda4a67ff63dc07752d057`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:56:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:56:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:56:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:56:28 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 00:56:28 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:56:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 00:56:43 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 00:56:43 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 00:56:43 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 00:56:43 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5d93aea697980315f27f81c68582d14f63dd3579c2d3a27dc495a588279eda20`  
		Last Modified: Tue, 04 Nov 2025 00:12:20 GMT  
		Size: 48.5 MB (48481056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:792d2002b8cc853f480f593dba17eee371d5be179d0452a4a71e23d7ba8f5157`  
		Last Modified: Tue, 04 Nov 2025 00:57:22 GMT  
		Size: 92.0 MB (92036049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ee21ee3bbfbf5138b1c25f6cf89d82e9f8bf22b30761af9d200d2ece5bc731`  
		Last Modified: Tue, 04 Nov 2025 00:57:22 GMT  
		Size: 81.1 MB (81147193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f334347865f5c160ab688041147da25f48151ea957130b992897f464cc83773`  
		Last Modified: Tue, 04 Nov 2025 00:57:13 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f4906e3d7a0f0a7d49db3a1764cf4c50f92a360670e494b6691c73c0eb3578`  
		Last Modified: Tue, 04 Nov 2025 00:57:13 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.3.1577` - unknown; unknown

```console
$ docker pull clojure@sha256:280bcbc81d90add3c35754a80583c438afaed5182f5e20a75c6e779085ec32b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7345311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1674138447c896c1ed2c9358e87a3b79026ff6ed5d84124eee006d2b3c5507d`

```dockerfile
```

-	Layers:
	-	`sha256:f1889a5b8c77bb7b1036f10b8b601e674851558e7546318029c618bcbdbdce5a`  
		Last Modified: Tue, 04 Nov 2025 10:45:18 GMT  
		Size: 7.3 MB (7327540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45e1d6807759500f42cbd71c10463d617e5e6ac41209edf0d7077af1ffa8af05`  
		Last Modified: Tue, 04 Nov 2025 10:45:19 GMT  
		Size: 17.8 KB (17771 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.3.1577` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:473b7c4d97f3eedb56167fe7e5bf37e16cd9cc1102dd3a17229a84c94ce41055
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.4 MB (220436712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5584afe526636283e23ff492c3ddcd2739b10bada6fd375c24e01d41f2e60da4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:57:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:57:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:57:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:57:10 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 00:57:10 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:57:25 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 00:57:25 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 00:57:25 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 00:57:25 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 00:57:25 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b81c3047c0240876c5be21e30ab0bb3930d31a1fc064a5cfe3b73eaec871a74c`  
		Last Modified: Tue, 04 Nov 2025 00:12:55 GMT  
		Size: 48.4 MB (48359478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8285005604231a3790f3a03385e1e6e24d730a2c1d943b455345657438963fd6`  
		Last Modified: Tue, 04 Nov 2025 00:58:00 GMT  
		Size: 91.0 MB (91045257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6185b9bcec984db83b97e9b6f3b58d90a7ffaf312b707ab47345c1bbce306b`  
		Last Modified: Tue, 04 Nov 2025 00:58:05 GMT  
		Size: 81.0 MB (81030935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6601275e7cebc62e34e75cb1ece2688c4488970a283f7d6fb4531b25b84015b4`  
		Last Modified: Tue, 04 Nov 2025 00:57:54 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97a191a06d34ac1bb52c48e8bb2419fffe2a82b7ead8a0e1491658731f69fd5`  
		Last Modified: Tue, 04 Nov 2025 00:57:53 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.3.1577` - unknown; unknown

```console
$ docker pull clojure@sha256:c8712ccaf4fd016a5563735acf22edde0bffd2c6a1e526eb9ab73da9bc884f51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7351333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7e08594f839728efc61df06c71a918dd012bab55ee1df362cb70bf042cf9755`

```dockerfile
```

-	Layers:
	-	`sha256:d5b18cfc355a05fa448816859bfda86b9a397a3451ae9941dabf460e88d7f463`  
		Last Modified: Tue, 04 Nov 2025 10:45:25 GMT  
		Size: 7.3 MB (7333372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ff3490aacef75ed559016f5807072ab2fd26c1b3f46fdb7dfc8f75f14295a85`  
		Last Modified: Tue, 04 Nov 2025 10:45:26 GMT  
		Size: 18.0 KB (17961 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.3.1577` - linux; ppc64le

```console
$ docker pull clojure@sha256:89bd3a9d61687c0a759d551d5c91096121cf68e583be8cb65ad109e649c45922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.9 MB (230916110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d807562ae6fe09d1f80644e7d3c0325a75d590a2dfc3131f556304f000563979`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:57:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:57:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:57:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:57:05 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 00:57:06 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:59:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 00:59:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 00:59:40 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 00:59:40 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 00:59:40 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:dcdb26575d996c21e1eb1166ca8252365548a95e0791c754c1a66e3abe07a271`  
		Last Modified: Tue, 04 Nov 2025 00:12:39 GMT  
		Size: 52.3 MB (52327280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697fd59e7c3bbc197eda379a24912ae560eb9e07af558ef7f46c037d6dbf5da3`  
		Last Modified: Tue, 04 Nov 2025 00:58:43 GMT  
		Size: 91.6 MB (91601697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3aa8eadc0245466bcd8d4ab024ab9ba8ee8b3f67d14af67fbe19d6adede01e9`  
		Last Modified: Tue, 04 Nov 2025 01:00:37 GMT  
		Size: 87.0 MB (86986094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865c0dd26cb70fc05528c1b018c07fd30b460a044273eb19844824b7d59d8019`  
		Last Modified: Tue, 04 Nov 2025 01:00:29 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b4e5dfd7101060a68216b59fe9b870ca8df49dec1f33f6c33858ad307c674e2`  
		Last Modified: Tue, 04 Nov 2025 01:00:29 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.3.1577` - unknown; unknown

```console
$ docker pull clojure@sha256:28d8a5dc7af2daf4f080f84949230c7c19307a2f0b63237e0d6e2c6b8b3dcbbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7351144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a078462f8207f266c788744ec6c518c883d60d3bf6fdd944e3930946144775ce`

```dockerfile
```

-	Layers:
	-	`sha256:267830ab33b86cfa79468502a052ba1f61dea188340e8d3de6f09f906163d428`  
		Last Modified: Tue, 04 Nov 2025 10:45:32 GMT  
		Size: 7.3 MB (7334088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df4220fac66bea9eeb41627610f6c09b34842f13c5c1d42841219427f18c89db`  
		Last Modified: Tue, 04 Nov 2025 10:45:33 GMT  
		Size: 17.1 KB (17056 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.3.1577` - linux; s390x

```console
$ docker pull clojure@sha256:834480a8904271610304466c9da126812ed732fbae5db27be79fe26bf00de57b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.3 MB (215302185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b889f9ca8e9546ee93da36cf245cb9c50a8dadcbd75d84d3acd786439077a0f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 06:16:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 06:16:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 06:16:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 06:16:46 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 06:16:46 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 06:35:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 06:35:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 06:35:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 06:35:42 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 06:35:42 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0a071bbc557d9d42732d58a1d6434bf94baf5f06b391c076c996395c193e41bf`  
		Last Modified: Tue, 04 Nov 2025 00:12:11 GMT  
		Size: 47.1 MB (47138093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a44c022f304dd76bdc7608befad5bc0f9a88754ecb1970943a535e7f9c6a8b41`  
		Last Modified: Tue, 04 Nov 2025 06:18:05 GMT  
		Size: 88.2 MB (88206432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4756c413d578f52b777de2ecd60eaf20441d76d07382ac815b561d20fac257fd`  
		Last Modified: Tue, 04 Nov 2025 06:36:26 GMT  
		Size: 80.0 MB (79956619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9eda067400dc28adc6cffe61427582df19b20a5ecf0fdccc64493cfc0e4193a`  
		Last Modified: Tue, 04 Nov 2025 06:36:20 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e3fb5c2875285c2d33bce347798e5d6b7da5e102eae7714c30728cfff0b47a`  
		Last Modified: Tue, 04 Nov 2025 06:36:20 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.3.1577` - unknown; unknown

```console
$ docker pull clojure@sha256:17c1ab450de848a632ea3b362f1937b3bbdf3325414c1ce55b8255b4fa69f07f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7338378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76bf781ec65a4e3312226ce9772c687908b06d8204ccc61b839153eb90995074`

```dockerfile
```

-	Layers:
	-	`sha256:13a5b5d074a1be88ab29fc3d5ffa876d464ef3b0e221919f78e081ab7c96475f`  
		Last Modified: Tue, 04 Nov 2025 10:45:39 GMT  
		Size: 7.3 MB (7321407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8ed3185c10fb1263d6cda91345727310420b5e8b1fe25284df14ecec506a932`  
		Last Modified: Tue, 04 Nov 2025 10:45:40 GMT  
		Size: 17.0 KB (16971 bytes)  
		MIME: application/vnd.in-toto+json
