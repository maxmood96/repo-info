## `clojure:temurin-17-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:73e627f8ca4a606eae5480ecd27717af3ebaece5a35abda581b60ecec97298a7
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
		Last Modified: Tue, 02 Sep 2025 05:50:59 GMT  
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

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

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
