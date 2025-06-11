## `clojure:temurin-24-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:b7fe573f8ba7a0446eba7bf16e3722808e93e42c9a3760994a4e7a837ee2e8e8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-24-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e2eb814b317371ca7640fe21e371a76f67ae3c45c27919dfb3e102c897b7a88c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.4 MB (191431400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2a881b2771b448defe593bd269a660e6c6e0db78376836eb346d821bbb0ad69`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1749513600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6f052c0ff895d860a8f6983dcf5207c5e8ff5949529101bf68c1e92e9c8baf36`  
		Last Modified: Tue, 10 Jun 2025 22:47:31 GMT  
		Size: 29.8 MB (29756816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05797adc8c500e1e24c2b27b5d7a490bd7b6b7ee01c3ea01546d2188ff0f76ca`  
		Last Modified: Tue, 10 Jun 2025 23:53:36 GMT  
		Size: 90.0 MB (89952003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57abe2830dfb91c22ac3389b50a0a5c5644e6c1ac7984b82d7fba640f78e372d`  
		Last Modified: Tue, 10 Jun 2025 23:53:35 GMT  
		Size: 71.7 MB (71721539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a7ac8614f1452dc4def8895f9ee9d727ae0fad6e94c893ea64764a2199e5f12`  
		Last Modified: Tue, 10 Jun 2025 23:53:19 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f4cbd2551f72abb213a8e28fa2054ea0ca0440dfea5d0e3d8b16b859069748`  
		Last Modified: Tue, 10 Jun 2025 23:53:20 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:500f3e7add9ff169ba29f476316b35aa237d9b400c48929e8d415662bc299d85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5219292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583e68beaf46ffe6097bc421e7134deacd28652b2a3206ab2ca9102ccb09b9ab`

```dockerfile
```

-	Layers:
	-	`sha256:f97c6dd68816e2fbacf7504fff95632421aae82a9b19cba9054166d0962a4413`  
		Last Modified: Wed, 11 Jun 2025 03:41:06 GMT  
		Size: 5.2 MB (5203444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5680a4fa1a98931319aae36ffc04b5e54af886ac541d03fd1b8c27acd4ec90d1`  
		Last Modified: Wed, 11 Jun 2025 03:41:07 GMT  
		Size: 15.8 KB (15848 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7cebeacfa5bd55b25eac1beaedb2bd979c9126a2013a9b9931b56651af2f6c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.2 MB (194179065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:144c8c34c13b8c04e950a4638d7f2aa5fccd3489252ab91732452eb23caf0a56`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1747699200'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6098c2c9fa277c00ab580ce12bf64a9e1edf9e9139ba18ad85f3cc3063834aa6`  
		Last Modified: Tue, 03 Jun 2025 13:33:56 GMT  
		Size: 30.1 MB (30119455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9eae18b910302d512424dc442cd7d56bf789911ad2568ced024da733788c71`  
		Last Modified: Fri, 06 Jun 2025 12:13:25 GMT  
		Size: 89.1 MB (89091283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0b38b5a2d2bc1f732a90620c22adf379f1a75f5c90fe9570ec412b0fc1b71e`  
		Last Modified: Mon, 09 Jun 2025 18:03:50 GMT  
		Size: 75.0 MB (74967284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f10e998f717f330d51060b0c5956f17aa7df01dfa0beb07905d935f0e4fd649`  
		Last Modified: Mon, 09 Jun 2025 18:14:39 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8973727016970b69df3a0721f95accad080a678e0362f5938fee406c3f01048e`  
		Last Modified: Mon, 09 Jun 2025 18:14:44 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:76b94288095bc19376a40086856766006cc3c4aa09248cd4c0c14267010c01b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5224662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaeb1d98be07a46d63741c72cdf1cc2ca7a3205e61361954d1a7f8aea7f177bd`

```dockerfile
```

-	Layers:
	-	`sha256:640ff86e2a7a8e9298f3c1b923478b57f6737422b80477d1ab010629dad91a7d`  
		Last Modified: Mon, 09 Jun 2025 18:42:07 GMT  
		Size: 5.2 MB (5208696 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88655a97fa42c579118580cbbd37b322bbebe50d36e9a97f488239ddeb7e242a`  
		Last Modified: Mon, 09 Jun 2025 18:42:08 GMT  
		Size: 16.0 KB (15966 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:69da32d7602a484173e539b37ae62decdfa211a1a8c2593e76f8c249e8a94869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.9 MB (203903635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83d93d90e38b3540be4870c6427500b9e2e514867839f1bafd27cf3e7e25a6c4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1747699200'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:62eecea9deba6eaccef3e829ddec51f2c540dbbb668a68816c8ce3c4b8023d93`  
		Last Modified: Tue, 03 Jun 2025 14:07:09 GMT  
		Size: 33.6 MB (33580565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9425324caed17cbe9579689cf7955835ba7b30d6602498824e5018dfaa80960`  
		Last Modified: Tue, 10 Jun 2025 11:53:14 GMT  
		Size: 89.9 MB (89920262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f663cd88e700309679cd6b6508c56ed196958134f0e2db308f9d225d26926fe9`  
		Last Modified: Tue, 10 Jun 2025 11:53:29 GMT  
		Size: 80.4 MB (80401767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ef37385f359aa20dad060a5d1083f0ecf9e44a7a81851f7960edd6f1a99040`  
		Last Modified: Mon, 09 Jun 2025 18:28:39 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a501e45666378d7f976fee754944693339d37056ad720327afe05be010fa8658`  
		Last Modified: Mon, 09 Jun 2025 18:28:39 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6eba5c13a9443fb3b697c230c9c9fc06e3f0087579222a9eed424659d90e1971
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5224495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2cbb719370cccda99a366f74d7a48c3ed475de6e1bbb3fdfe1edf8a65f7f17b`

```dockerfile
```

-	Layers:
	-	`sha256:4675876744e4cd0b4936a85305bb8ef15f5c1828f86c2458095d6d8fea293a94`  
		Last Modified: Mon, 09 Jun 2025 21:40:09 GMT  
		Size: 5.2 MB (5208599 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:307a08f177864c34f8502b2ac7594f3fd6adb8a48e4f7e4c2df70b24deca4f6c`  
		Last Modified: Mon, 09 Jun 2025 21:40:10 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:021eda093c7a9646aaa682533a9899a29f848856f9f6cf29a4f4986229f5ca71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.6 MB (186584067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f580f1a754896a92a9f24c9f72831c8e8ec391f23a5792c6e53770580774d727`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1749513600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3a4ce3b49438d6e971d6a25501e5ee98899a309dea36cc03fae31602fe4551a7`  
		Last Modified: Tue, 10 Jun 2025 22:57:56 GMT  
		Size: 28.2 MB (28247070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a09b883acc3f8428b9c4a6efa04367b7b31096d2a081942d7e9869aa32ecf132`  
		Last Modified: Wed, 11 Jun 2025 01:20:38 GMT  
		Size: 87.6 MB (87622163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34566a4f14852d44d5c4ff12e84806122c5baa423855e43d829d61b4283092f7`  
		Last Modified: Wed, 11 Jun 2025 01:34:37 GMT  
		Size: 70.7 MB (70713789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7285f877b22136cd22ceb8bb9f24778c3e3273acbed27756a6fd67061f1d1c22`  
		Last Modified: Wed, 11 Jun 2025 01:34:31 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cc44e68107ff1a0a07955ee2f5d1903f15201f8961f22e71b01fda6542eea74`  
		Last Modified: Wed, 11 Jun 2025 01:34:31 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7d7e6ab2c8b30615c5a5a26caa5c85535eca5933f717482e715569835e4c9ffd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5208800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0176b88efff133eed6f948bab40bee34ed737e6f5c1583ae0085495ed261c85`

```dockerfile
```

-	Layers:
	-	`sha256:f09bdca696eb7be98a466f5eb883beed65aec0e6d3e9f2312845e2e8d10f9f6a`  
		Last Modified: Wed, 11 Jun 2025 03:41:19 GMT  
		Size: 5.2 MB (5192905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccc8595ac21638fd9a1167e839da7fa4473353361bcb993e319996519ed37db1`  
		Last Modified: Wed, 11 Jun 2025 03:41:20 GMT  
		Size: 15.9 KB (15895 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:2fc18e0d41fd1d1aa3ee862f6e63bf2bb32ed30395c5a135170ea05c95ef11d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.5 MB (190453335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4160e4d8b9fa17675c36f33eb3b1556a5c50352b71ddaac1eb11e7c53ef2dfe`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1747699200'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7cbda353d6047374e3da60bdf79ae89f8047840010f0964c87a8f2714e146106`  
		Last Modified: Tue, 03 Jun 2025 13:43:57 GMT  
		Size: 29.8 MB (29829620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e16c52945849bd7ff81f8fad1acf7f6b275ebd424116d7c5e5b466881d6e648`  
		Last Modified: Wed, 04 Jun 2025 04:21:26 GMT  
		Size: 85.2 MB (85216842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8da4062761b72bd73bcea3cc5726b8269be668d7b9e601d976e6ce52ecd399`  
		Last Modified: Mon, 09 Jun 2025 19:02:10 GMT  
		Size: 75.4 MB (75405829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95292178a946714afc3183a980a5230add7e82d010f570d484887cecb319d4e`  
		Last Modified: Mon, 09 Jun 2025 19:02:02 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d575a1cc6fe9c92d0a7f7e556d59415fa27beb5f1382facd3f5f1dede316ccf0`  
		Last Modified: Mon, 09 Jun 2025 19:02:01 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:90e3bf23b827ab2fe87ba844d5c69660f6677e63bfc054111bed2865e28194d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5217250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:540c636439d50430d2162d6d1f98acdff03890d5d846075d63ff2868de178b09`

```dockerfile
```

-	Layers:
	-	`sha256:4288e597b00180c24bd9453d47fb879d2d894239d0432cc8257f1a26ac3ce939`  
		Last Modified: Mon, 09 Jun 2025 21:40:20 GMT  
		Size: 5.2 MB (5201402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ed64393fdf601f55ebe35a65645e26d78a6d4bb1c44c0c2fa0e730a1f960608`  
		Last Modified: Mon, 09 Jun 2025 21:40:21 GMT  
		Size: 15.8 KB (15848 bytes)  
		MIME: application/vnd.in-toto+json
