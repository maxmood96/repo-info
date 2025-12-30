## `clojure:temurin-11-tools-deps-trixie`

```console
$ docker pull clojure@sha256:ce9d8acced635dde63fb9628579c966ac68c01772e4ac2b6e8e48e52b5bd9d98
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

### `clojure:temurin-11-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:68073f68d641bb69d35aad9bde7990fa9d004511bc3a6c514b98d206db6c0030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.8 MB (279799579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9078ee352c8188ca2b7dfaa997730d4430c927d69e7289b6b5c81253543b5a2e`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:56:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 00:56:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 00:56:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:56:41 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 00:56:41 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 00:56:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 00:56:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 00:56:58 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:281b80c799ded5b9a390d2e8c59930db01ee395ab809dd34259897c660751f4e`  
		Last Modified: Mon, 29 Dec 2025 22:31:07 GMT  
		Size: 49.3 MB (49289587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e837d41a4eb898dfa75d7137c4ee9c524d3d23a675ef96779069b557dfe13e54`  
		Last Modified: Tue, 30 Dec 2025 00:57:41 GMT  
		Size: 145.0 MB (144966608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62730e7ab671eeb5664e6ca554aa01c1fbd4a5c9d210a846a75fc3f0c494c070`  
		Last Modified: Tue, 30 Dec 2025 00:57:35 GMT  
		Size: 85.5 MB (85542740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50389c739548009e15ede1b95c13271dff7c6da5b218a92263aed809d9b50bdc`  
		Last Modified: Tue, 30 Dec 2025 00:57:27 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:0c0420d953b0be20a6bd03e7a9959cfd0ccbbd3d7c6cb73a21b23ec6ae50d8ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7501255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd04386d14407e631b9e7f9c9daff6ea2a23cca295def362ba509b0aac3d7aa0`

```dockerfile
```

-	Layers:
	-	`sha256:b1537cf773111c894cc56baedb7c366dd2983f31508ee98992dee739eb480502`  
		Last Modified: Tue, 30 Dec 2025 04:38:34 GMT  
		Size: 7.5 MB (7487070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7085855e566e89afda6ec2d532e6151fea8c51c6515d4aa8cd6c4287af5252c2`  
		Last Modified: Tue, 30 Dec 2025 04:38:37 GMT  
		Size: 14.2 KB (14185 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0aa0efec78c98d9e1c4ee95951b58f71ac0948dc3844aebd2f97b6c04c8fdcec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.7 MB (276743791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4778a95f8d2078ecb622f8b85e13698b810928526378e65c5ed224b64eda784`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:57:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 00:57:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 00:57:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:57:46 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 00:57:46 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 00:58:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 00:58:05 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 00:58:05 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:5785abec2864dcd8d343ccd872458a50ffb2a61739bc46a79709c68c455cb8fc`  
		Last Modified: Mon, 29 Dec 2025 22:30:57 GMT  
		Size: 49.7 MB (49650193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78692600cca7ae534036f85abe371157893f258d4dce47b8612b11b472f4a208`  
		Last Modified: Tue, 30 Dec 2025 00:58:50 GMT  
		Size: 141.7 MB (141731577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecdd249dcaf8476f87994bd7fde0ae2a876c9075e58382082f5a6f45612ba919`  
		Last Modified: Tue, 30 Dec 2025 00:58:43 GMT  
		Size: 85.4 MB (85361376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b95e592f1dc18ad4f6eabb542e6a9e27ec4b9b2b5fb0840f302f5dc41928c41`  
		Last Modified: Tue, 30 Dec 2025 00:58:35 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:cb3a65ec93383f22315f36d86d4f5c4933e36bc1cb4814f4fb8dc2f59aad9552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7509019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dac2c8d7c6081cf2e1fbb043b10bf2b71f199c86e6a0461322dd10f430fa62e`

```dockerfile
```

-	Layers:
	-	`sha256:052a7e98943b47e8991ddf354fbcc0d45700afaf30e895a3057bb2d207b4e349`  
		Last Modified: Tue, 30 Dec 2025 04:38:42 GMT  
		Size: 7.5 MB (7494718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bf0e82c9f49598f7bdb70f0fe0af800b1569a1eee795bf68928311a4a9c07b5`  
		Last Modified: Tue, 30 Dec 2025 04:38:43 GMT  
		Size: 14.3 KB (14301 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:257542df661f4fc1ec595e84f5b8751bed0b1a890255a4684cdacd00286ef3cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.1 MB (276136263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c78b9418026399adfdd6987863772c09ccc097a366d50747ac61678047db267`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:25:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:25:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:25:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:25:25 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Mon, 08 Dec 2025 23:25:26 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:52:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:52:04 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:52:04 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:fb00391cdf4b5dc5fe2e67e0bee3770076e9af9efed48ba15cb306902e36c78c`  
		Last Modified: Mon, 08 Dec 2025 22:52:23 GMT  
		Size: 53.1 MB (53108478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37d1cc451357decc266df875d9334bbd4504581a335e8cd24c32ce8844bcd57`  
		Last Modified: Mon, 08 Dec 2025 23:26:56 GMT  
		Size: 132.1 MB (132081948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168d6c6f2f67c7ddfb21fbe127a2dd89d1f629c89eeedd8082a23cb46a0581a0`  
		Last Modified: Thu, 11 Dec 2025 22:53:09 GMT  
		Size: 90.9 MB (90945190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d034c0e4809f4bfd8e0d336e77a5b7c24168dd8f871b7a95e7331eb3a0607a33`  
		Last Modified: Thu, 11 Dec 2025 22:53:03 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:6173ffee61976a3f29fda3b6106572da88a203200cc8578d5f154e57d7b03894
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7505107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:125cacbef7c0db4aac224f1d241c4f0aff42963e740cfbbd00cd05ee16b6135d`

```dockerfile
```

-	Layers:
	-	`sha256:6989470e7d13294ffa44c96010059106a1215edcffd0dde7edde256457cdc7c3`  
		Last Modified: Fri, 12 Dec 2025 01:36:58 GMT  
		Size: 7.5 MB (7490874 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a29c7ef641a786f18546ffe042ab0e8ece99ec3d06d4719c957d64bdb541bdf2`  
		Last Modified: Fri, 12 Dec 2025 01:36:59 GMT  
		Size: 14.2 KB (14233 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:020c26f9bbc9905a194c450425d24f267c289c53d208aff08fd39a03d8b04166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261549605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd818a6583ee1467ec4dba5369ab80877bacecec71cdd6803edb1a6cf6d3eb04`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Thu, 11 Dec 2025 22:33:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:33:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:33:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:33:03 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:33:03 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:33:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:33:19 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:33:19 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3f8967bef2f6a8ec916f7d3a0d528a6724093176621c5758addeeece50e41dec`  
		Last Modified: Mon, 08 Dec 2025 22:16:15 GMT  
		Size: 49.3 MB (49345908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179e7c978a5c9b16756c11984d3e35b7b98189223b21d5ca750af0a4063fa46b`  
		Last Modified: Thu, 11 Dec 2025 22:34:16 GMT  
		Size: 125.7 MB (125694399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c511c3a8a3105cc77312310c5d00e326d87f42a339720990f033cb30e9f5528`  
		Last Modified: Thu, 11 Dec 2025 22:34:09 GMT  
		Size: 86.5 MB (86508652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4f527c6070918282c8c00bf54624a552988fdc73fc7c894fb7de39f08a0807c`  
		Last Modified: Thu, 11 Dec 2025 22:33:56 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:15ed2ea22fc3c883a49345e1017f61c912f9c95e57ee9d68b44850ea7ee6d767
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7497181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe3927f57385a931a4bb58304534d12f30482f1ea8fdfcf0943e0607f06480c3`

```dockerfile
```

-	Layers:
	-	`sha256:de99bdd42a59c43ebaf608499b4aabaa50d4d0fd34c9d25658003d5705c116a6`  
		Last Modified: Fri, 12 Dec 2025 01:37:06 GMT  
		Size: 7.5 MB (7482996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c33eeaca0ee4f2136e1179ab3c7ddd96e089631614a9b63a2f5eeaea3a93563`  
		Last Modified: Fri, 12 Dec 2025 01:37:07 GMT  
		Size: 14.2 KB (14185 bytes)  
		MIME: application/vnd.in-toto+json
