## `clojure:temurin-17-bookworm`

```console
$ docker pull clojure@sha256:fa3b69c08a0bf8f65ab12d778fcb7161ba9b00c1a341326611145030d7cc6d15
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

### `clojure:temurin-17-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:5587d61bd36548c31c056a0fc1c817027b8ff4dc843e58a352b94d119b9eaf74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.3 MB (274326933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6134d0ea5e83bb305e5f9618651566462794c86ae51afec90f503642bd36bf9c`
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
	-	`sha256:2b89d24929f581a5bbc25f56ba2032415e33a41360c49fbec3501accb5e4913c`  
		Last Modified: Tue, 02 Sep 2025 00:17:43 GMT  
		Size: 144.7 MB (144693327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d577a12c8819cea3b66c96bbefbe2a9ff2008778c3c4b67ba3506b2c74c852`  
		Last Modified: Tue, 02 Sep 2025 01:57:18 GMT  
		Size: 81.1 MB (81138051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b78301f2d5090420e8c5f7f2a100115fdc67a70fa4aa1fe4af4ab8590e27d50b`  
		Last Modified: Tue, 02 Sep 2025 01:57:12 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b50649903c13392e612e37a4976d16badfe82ba61a54e284d2436e7482de32`  
		Last Modified: Tue, 02 Sep 2025 01:57:13 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:9e12d52457e100c8d87ac7a52c8a62470ec4ec669ee4871347780add9498f910
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7384118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfdf65cb84889ce8e6dc2a00c717017b0aa290b594cc9154df2b519b6c1dfa29`

```dockerfile
```

-	Layers:
	-	`sha256:23f70189741dff3530166529d705409ea0e4658044e3fa6647996e7b5926b83c`  
		Last Modified: Tue, 02 Sep 2025 03:37:58 GMT  
		Size: 7.4 MB (7368297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:667b5c320955ed096d965e93968041fa43e641fa6621feabfa92d85d09d0bd1a`  
		Last Modified: Tue, 02 Sep 2025 03:37:59 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm` - linux; arm64 variant v8

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

### `clojure:temurin-17-bookworm` - unknown; unknown

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

### `clojure:temurin-17-bookworm` - linux; ppc64le

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

### `clojure:temurin-17-bookworm` - unknown; unknown

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

### `clojure:temurin-17-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:4b1b9290b05436b50832e84712de9cf6e6def53d8f6e53d8fdb25b07cc2d594c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.8 MB (261828954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ff1d731de558973b27fc8b6a87cc577017be7eb1f94ebf43d80f5f9b79759a7`
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
	-	`sha256:b10ba714af2b17b160164d154f0543b7958396c5663a80a4dae32706aba049d1`  
		Last Modified: Tue, 02 Sep 2025 01:56:43 GMT  
		Size: 134.7 MB (134724244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3849b782ca4263d036bc5c708dbf22f736b7481e2a3b9a5377c2a13a6c3dadf7`  
		Last Modified: Tue, 02 Sep 2025 02:02:55 GMT  
		Size: 80.0 MB (79953804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da17fe646ceef0670f17fcab1f3a5090dab0bd373cb310a8febdc7d2efcc88c`  
		Last Modified: Tue, 02 Sep 2025 02:02:50 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f39e70730fab3d864c94e23a077eec8e6a1c537e4b995bf6517cfe87d078842`  
		Last Modified: Tue, 02 Sep 2025 02:02:50 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:158dd90df622c1f7846e1e8ae8bf554c5317a69093ffc41b08df73610c782879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7375436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:821692bcf90bd1da84adc531b3fc3660eba0aad3a7ca3298605faead553a8807`

```dockerfile
```

-	Layers:
	-	`sha256:de5a524ae693a72c7db52e90d097460daea6618b291aac54abd7b8b93375f87d`  
		Last Modified: Tue, 02 Sep 2025 03:38:16 GMT  
		Size: 7.4 MB (7359616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a89f06508f0332af9f817fd16a0aa287b93079cc116032e00d9c24ee365ff378`  
		Last Modified: Tue, 02 Sep 2025 03:38:17 GMT  
		Size: 15.8 KB (15820 bytes)  
		MIME: application/vnd.in-toto+json
