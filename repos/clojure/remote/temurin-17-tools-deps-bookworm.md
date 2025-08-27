## `clojure:temurin-17-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:9c9ff01f102536401098f7a13e94045e94dda63a7512d60376f9ef51d9bb1f60
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

### `clojure:temurin-17-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:5c984ef38d21418d86781c2e82f3b55f36134007e7a261cec3d9cfde763e1874
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.3 MB (274327333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68b332bfc3efa5993505b565da70a27a650230f09ce5aa184c5ee9ec4e2c3c31`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f014853ae2033c0e173500a9c5027c3ecffe2ffacbd09b789ac2f2dc63ddaa63`  
		Last Modified: Tue, 12 Aug 2025 20:44:32 GMT  
		Size: 48.5 MB (48494511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7fbbaef372ac85cd0e0d486e3e7d3864ac7582a3665a9754715557d1a0e419`  
		Last Modified: Tue, 26 Aug 2025 23:13:10 GMT  
		Size: 144.7 MB (144693301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c6ddde37a663feecb709394f35ac5e15e0360352f04abf71468cf521a8e2ca`  
		Last Modified: Tue, 26 Aug 2025 23:13:01 GMT  
		Size: 81.1 MB (81138478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c06660cc26fa2b2abbec4b464d17255f85b02a8a2b026fb0bb4f2b9195bffd79`  
		Last Modified: Tue, 26 Aug 2025 23:12:58 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35126b974ca3d8415b1252833641f24fe8ffddf4ced6774eb4bc1473293fd16c`  
		Last Modified: Tue, 26 Aug 2025 23:12:56 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f10af82991ca4f82905655c1516636df9a3102b3c102bae40d446fe9ae2f89ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7384118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ada672620c07011e196490ffa585c5c926ef4286d1605650c480b8e9428a0a06`

```dockerfile
```

-	Layers:
	-	`sha256:3df481ce95e68e2561f42fdcad5b1c1c0f2eeb81a947ce403acaddfe6e0d8e52`  
		Last Modified: Tue, 26 Aug 2025 18:37:20 GMT  
		Size: 7.4 MB (7368297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b382a5467916c7c5bceec805a83aabd86ad19cd49a32f113f6c22b09673f981`  
		Last Modified: Tue, 26 Aug 2025 18:37:20 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:82f9fb136b11f7fd6108ee77bcdfa9fda1619c770648e74d40e9dd463690f404
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.9 MB (272895059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5932964f9abc67f6c030a86731ddaab38e93669112a7c341aa252701439ff091`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:35f134665ae4469a16b5b7b841e9efe6b186960e0533131b3603e4816aabeb3a`  
		Last Modified: Tue, 12 Aug 2025 22:08:09 GMT  
		Size: 48.3 MB (48342450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909e393deaae408fc3b41edb2a8ab7e1c60d9829c199ab0b73b6ef3527e54b3a`  
		Last Modified: Tue, 19 Aug 2025 03:52:07 GMT  
		Size: 143.5 MB (143542112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c8d756dbd0371e7f0c3532daee42ba1615e1f6dd487c80256c7db2c4990c5e8`  
		Last Modified: Tue, 26 Aug 2025 17:41:24 GMT  
		Size: 81.0 MB (81009452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb6b293fe6b17fd531678ca79657fb2c346c940af8375406248cbeeea7aa2b9`  
		Last Modified: Tue, 26 Aug 2025 17:41:17 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054521f703d8c2781b12714818d45fe88c62e2e34cf34835c4b0b3cdfaede966`  
		Last Modified: Tue, 26 Aug 2025 17:41:17 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:9abf37a44d9d346be306cebaa830f71a62b8d0eb4097428f7397907969577c1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7389999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bce91fee1e4fa86f10405830f45e930d5aa64a061828985c2972fa6fd5cca3ce`

```dockerfile
```

-	Layers:
	-	`sha256:4ec8f169b1c485b9cd7ab99952dc86bbd4f9a9d13afe8ba33a9e37953d03ac1f`  
		Last Modified: Tue, 26 Aug 2025 18:37:28 GMT  
		Size: 7.4 MB (7374060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3f3d0947e3e1f5e349dce594a46507b635f200dc5b0322990ca354b87223413`  
		Last Modified: Tue, 26 Aug 2025 18:37:29 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:2b5ec6f485f84133b529fafe628ab1b2c7aca137713f993c381b6f5a1c92f981
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.7 MB (283684488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82fc35e725a5074f240910ccb85ddf3b2d5d642115a1327cb701a561b799934`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:33bc01697f2fcceb00fe53fe1bf433b48dc127c82c1555f61eeddeda9d72ff40`  
		Last Modified: Tue, 12 Aug 2025 23:05:53 GMT  
		Size: 52.3 MB (52338077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ffad487e544c77a0c7de7f0d0d5d00c797145afe37087c25e8c9d92f650b6e`  
		Last Modified: Sun, 24 Aug 2025 06:15:29 GMT  
		Size: 144.4 MB (144372796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3049167c3a701ca42aaca64fe86c96a23b3a353e793ff1168a525c2d081897`  
		Last Modified: Tue, 26 Aug 2025 17:53:24 GMT  
		Size: 87.0 MB (86972572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea5e8984717594239288f5137378d53d735bb756c3aa9b0369925c637433f39`  
		Last Modified: Tue, 26 Aug 2025 17:53:13 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8f4685f18cfc736a2cf869052d3846b72eb13c19d7212055ef96da32282ddf`  
		Last Modified: Tue, 26 Aug 2025 17:53:13 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:8cc08f96412569ef4e7f10c210d899a405a495a27af548d56765992a2cfe4880
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7389370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15507397dd88ac1aab3fc7cd8c4861e861045f3aaee7ad4a731c1b8cdaf148e7`

```dockerfile
```

-	Layers:
	-	`sha256:91dfa1be6d7cba9d0ea7baa53dbac943ca604a0ddaa7c2e7c41832d6bb24c34d`  
		Last Modified: Tue, 26 Aug 2025 18:37:36 GMT  
		Size: 7.4 MB (7373501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1bf8c945e42bcf88b36c703a92c9b46eeef7d926339b768da540e13a43cb0a2`  
		Last Modified: Tue, 26 Aug 2025 18:37:37 GMT  
		Size: 15.9 KB (15869 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:8748c9357598cc076a4eec3a61bef360262be4003769fc963074b80afaf798c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.8 MB (261828950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6249903e2e5e54e42d62e420bd0147c25b62489472dec37dca305673f51b237e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:635b31fd21bf059b6af0abf57b343066d0218ebb3e0b679927cc1752427a72da`  
		Last Modified: Tue, 12 Aug 2025 20:53:37 GMT  
		Size: 47.1 MB (47149866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:965fc491c1e3266f9106d3cf6129a94088b309c79bb586330bc19c70b371f92d`  
		Last Modified: Sun, 24 Aug 2025 06:15:47 GMT  
		Size: 134.7 MB (134724418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8678e6a64e1e29f6b8d4ca3f1a0d00835ca26c9ef854842b594afffd40f49889`  
		Last Modified: Tue, 26 Aug 2025 18:06:25 GMT  
		Size: 80.0 MB (79953621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05eab3dc2b5cb05e63daa3c15fd4f7068c20b1dfcff1560d8d73d5e2d2c1fa87`  
		Last Modified: Tue, 26 Aug 2025 18:06:13 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47813838fa02b7a24bcab3e59f4df0c9cec0f42571ed365a7e6563f3ad2e4627`  
		Last Modified: Tue, 26 Aug 2025 18:06:13 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:976c00959beeb0c0a2c61b97cdea0d4b7b1e6d22bc5103520c0b2a04594abd29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7375437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0f59869eec917eb2563485f078f8f9c8e29ecd15be7d63633bb95d161b7de96`

```dockerfile
```

-	Layers:
	-	`sha256:ec0736f410caac732103a363a1d1829835aa349998afbcd64765b632d01e2920`  
		Last Modified: Tue, 26 Aug 2025 18:37:44 GMT  
		Size: 7.4 MB (7359616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47bb417072ec8959c797f11e25f87b7cc935a51737074e86a6828457874bdf25`  
		Last Modified: Tue, 26 Aug 2025 18:37:45 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json
