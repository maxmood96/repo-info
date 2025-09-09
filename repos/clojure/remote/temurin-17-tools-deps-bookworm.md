## `clojure:temurin-17-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:81f12cde49f7a2ec3a887f8581a8a8a3ca257a9b203ede37b592810bf48f2d5d
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
$ docker pull clojure@sha256:bca7d5e8d05152a16a17978a4ea2c89a053a3f05e315100541ada8d38131e828
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.3 MB (274312607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b58a8cb0cc6bd150be55bdbf374b7a9667d5086ffe945bfc3d16bd4ede9bfd3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b3669f7aa7e696e209f2edd6209a18e3dc65562a66fb051d488422e00fe0b2`  
		Last Modified: Mon, 08 Sep 2025 21:43:27 GMT  
		Size: 144.7 MB (144693322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c9450a24f9aafc4526d3f8173bbd1c89f1f3528788cf3d59eab1ad757ef1daf`  
		Last Modified: Mon, 08 Sep 2025 21:43:26 GMT  
		Size: 81.1 MB (81137636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f32e16ae1495a2538e8c91283211fd7b7a0e3e95f7e139e20fc48992ba87a083`  
		Last Modified: Mon, 08 Sep 2025 22:31:35 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:214fe8d6c15af241b6f896aa38c842ea4f093743ed8ac60876b8f1e0d6f58822`  
		Last Modified: Mon, 08 Sep 2025 22:31:34 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:e86d90781d80d84fbfb49ae8ac0d297e66f476a4c1d04915aa022c2cfc7d8843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7390710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:197fac1b8b22ce472e2634676cce70f382216d927c57635a45145c54c88fc627`

```dockerfile
```

-	Layers:
	-	`sha256:a3e0321a948c52b0071e60d43ed15f0eb0b0ddf274ffc56dadcc541869606d45`  
		Last Modified: Tue, 09 Sep 2025 00:37:31 GMT  
		Size: 7.4 MB (7374890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9b375357d3bc35add81fbe42021dbede1b172c96ee4bbc1914a4c48ce68011c`  
		Last Modified: Tue, 09 Sep 2025 00:37:32 GMT  
		Size: 15.8 KB (15820 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:334bba374b7dd0dee33cfb9bf0583f540bb7d971ce0a20c594163c30c49d0876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.9 MB (272894965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efbc8f0ab8c335da30b49ce9b2cbaa6f0952914799ad60a3e9396478268e646c`
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
	-	`sha256:fa38b1c45ce90f230b61f0adcdd7e2f359033689f5bd207abac0a654d0abdd85`  
		Last Modified: Tue, 02 Sep 2025 09:58:16 GMT  
		Size: 143.5 MB (143542156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af08a9abce9573a32920aa360802ca209b97e9c6aa548a41a828e5632f8342e`  
		Last Modified: Tue, 02 Sep 2025 08:04:00 GMT  
		Size: 81.0 MB (81009315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8502bade97a0eec77beecc8a062c9e0441819bca29d2292f2b1e627ae99fbdb`  
		Last Modified: Tue, 02 Sep 2025 08:03:52 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d3e8d28fd36383dd1552df05b6acf9269bf2d71b7905c830beb74e4521aa36`  
		Last Modified: Tue, 02 Sep 2025 08:03:52 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:dc1082b3521462d2cfde52402dafd8c5b91e1412d83cafe5de68e127e047d110
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7389999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b349874195edf9b715f856ea3932d27f610a9eccd7c716b1d1a70e3623d818c`

```dockerfile
```

-	Layers:
	-	`sha256:33d8b2a82640cd3911cfebc85d8c0a643172e58dc89f7a40376befc0d0c895c0`  
		Last Modified: Tue, 02 Sep 2025 09:37:51 GMT  
		Size: 7.4 MB (7374060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed5a6741f037a1e465bda6caee3924b2f98d335850944e8285bffb06264914e4`  
		Last Modified: Tue, 02 Sep 2025 09:37:52 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:1bcdb900f92dafbae67022a8b275516cc85ddeb6a41b8853ff7220c1f7a8ec0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.7 MB (283684417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c550698d78ca48680e93893f5ee55f65109455d567d10c4759cc5397eb7b0bb`
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
	-	`sha256:328c693b6b84170d769c3dd2aecdfdd27d9e424c8f7591eda77da48b68918e55`  
		Last Modified: Tue, 02 Sep 2025 08:30:59 GMT  
		Size: 144.4 MB (144372649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5e6fe1767d28ef2ce1927b50296f6b6271333972db3ae04f0817f792af8209`  
		Last Modified: Tue, 02 Sep 2025 08:43:08 GMT  
		Size: 87.0 MB (86972647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957c1b84251aebd9ab53d2e59b0b0afa1f86b52f8584d6c0cacd7f6982f386dc`  
		Last Modified: Tue, 02 Sep 2025 08:43:01 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b3d7ead1ebb08d30d9f5539ed9134b8c57d8b38d873ab457eaab7c9f381612`  
		Last Modified: Tue, 02 Sep 2025 08:43:01 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:44b2215ddcc0a3a6f30195c12f22589c295901d434bf4cb28a13419f69fabcae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7389370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86b195e3596076453fc533d3927e4010061d72f4f55e4297e8564295ffdded99`

```dockerfile
```

-	Layers:
	-	`sha256:14067523f57808550893ea19f3d0bccfb103dad53b8f589a43ef518167a6665c`  
		Last Modified: Tue, 02 Sep 2025 09:37:57 GMT  
		Size: 7.4 MB (7373501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:418d2d56b61844548094066a82a3ee231fd58eb3ad530a014c552178e7698f05`  
		Last Modified: Tue, 02 Sep 2025 09:37:58 GMT  
		Size: 15.9 KB (15869 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; s390x

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

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

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
