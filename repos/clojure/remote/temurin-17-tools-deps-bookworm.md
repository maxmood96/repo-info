## `clojure:temurin-17-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:29c92a5a91ba2c331016043c7610437ea1dc6ec1819449d0a099e1c0b3f83149
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
$ docker pull clojure@sha256:bba7b0137566e370681abb2dc90a84d70beb76d3062cc8627828fa4c5481f4d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275268835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ef1bb053238c252646bd0b0a38edca012206739569e234023b5aebd371fae4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:54:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:54:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:54:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:54:59 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 19:54:59 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:55:14 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 19:55:14 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 19:55:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 19:55:14 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 19:55:14 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cde387eb91f78f5d1a862944eeef301640d3c10ec942c4b96ceae697bd9bfef2`  
		Last Modified: Tue, 24 Feb 2026 19:55:35 GMT  
		Size: 145.6 MB (145628702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d174829e61f30147e65039570303ad3eb72a237799c6cc59c761d3e57a1046d8`  
		Last Modified: Tue, 24 Feb 2026 19:55:34 GMT  
		Size: 81.2 MB (81150318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8633bc8d5f6aac34324e8e16f56665db9e611192d6ab01e151ba5fb89162253`  
		Last Modified: Tue, 24 Feb 2026 19:55:31 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2aa621e82912ab9e80f6ed0dd640fdf898acbacdc7c3507dca00587cfcde86`  
		Last Modified: Tue, 24 Feb 2026 19:55:31 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:40de46a1053fa424ddb88e0a59bcbe04d611ef5a09183e850b17f30a2e041fba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7392567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2356149013124442ac0cdac5e9faf9f4e87454c473d2865b7a7c851b67a8257a`

```dockerfile
```

-	Layers:
	-	`sha256:4183531419d3311230f230912ddc8fba06af457adb480ec9d63ba093a15895f1`  
		Last Modified: Tue, 24 Feb 2026 19:55:31 GMT  
		Size: 7.4 MB (7376789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cd892416fe2ecd4fd59eb000437145a6aaaf0be427bf962d78bcde5f7449d9d`  
		Last Modified: Tue, 24 Feb 2026 19:55:31 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:deab60d59376aedc93428ef2a3ecfbcfcda810b630fb940b7b21adf7cfd5ff7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.9 MB (273948765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34fae5f60ea91ec3d051d91be5e18f26882805727a295ac594ab2fdb95222cf9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:05:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:05:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:05:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:05:44 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 20:05:44 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:05:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 20:05:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 20:05:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 20:05:59 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 20:05:59 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8578011282ae3fef36307f7e3afb2265a96bada1a57648f07bea9cc1a11e7b7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:06 GMT  
		Size: 48.4 MB (48373210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00cbaee4f23c8e61222463cb0c3e7e598081dfcf5feec098a5558f0953658fe8`  
		Last Modified: Tue, 24 Feb 2026 20:06:23 GMT  
		Size: 144.4 MB (144436198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9894895dafec59a065a76c9673fd4a03b83b13e9ce6e50507f3dafc705be709`  
		Last Modified: Tue, 24 Feb 2026 20:06:21 GMT  
		Size: 81.1 MB (81138319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:219ddaf9fd31cd97b8c1c887b53cb93185fa74efcc1bfd1b35cf92680f190522`  
		Last Modified: Tue, 24 Feb 2026 20:06:18 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f0c247655838499b8879464fb147ef038165b7d968cb9397082ff16f8f20e1`  
		Last Modified: Tue, 24 Feb 2026 20:06:18 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:7e98b3d2927615601c2442766a77e64bf0fa815c40c5fd79b128679d57924a9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7398446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a0dde80428eda4be8b6ad0134bcf2851c280db7e215b120ed1eed652fd178cc`

```dockerfile
```

-	Layers:
	-	`sha256:505c8a9593de0545166cddd29b182efdd7886d06dcc2d606782f0e3168eb5786`  
		Last Modified: Tue, 24 Feb 2026 20:06:19 GMT  
		Size: 7.4 MB (7382552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4a7574fcf52d8308375827a9f7b8b5f76ffe41e78c15860c92a9aed0eed4072`  
		Last Modified: Tue, 24 Feb 2026 20:06:18 GMT  
		Size: 15.9 KB (15894 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:184d80a59155c79b31c737817294030309e378e096181c20102722232b59af54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.8 MB (284763154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:610329971cf9d023c9ca009502ddbe6d8579d5b86c802f902357b0b52364cc71`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Wed, 25 Feb 2026 01:57:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 25 Feb 2026 01:57:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 25 Feb 2026 01:57:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Feb 2026 01:57:27 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 25 Feb 2026 01:57:28 GMT
WORKDIR /tmp
# Wed, 25 Feb 2026 02:02:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 25 Feb 2026 02:02:24 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 25 Feb 2026 02:02:25 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 25 Feb 2026 02:02:25 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 25 Feb 2026 02:02:25 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:605d3e8e339092bb5c341e87f55fee22f143aaa738eb91d341b5fc6aa27b2b5b`  
		Last Modified: Tue, 24 Feb 2026 18:41:51 GMT  
		Size: 52.3 MB (52336797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad0aa6d34d02956b4dd5d0e851f2871b9952fe294ac6bf261a9b69647625519`  
		Last Modified: Wed, 25 Feb 2026 01:59:14 GMT  
		Size: 145.4 MB (145438176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64028eed6531062cc4ddba71ffba34fdac372d6aef75db75bbf326c11616df91`  
		Last Modified: Wed, 25 Feb 2026 02:03:13 GMT  
		Size: 87.0 MB (86987137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3759c679d085e9f9a57ade59b64ff477a43e3f9b1bba12915a05f67dd7a745d`  
		Last Modified: Wed, 25 Feb 2026 02:03:10 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecbc04c7009ab48e10021d2b56388b79fe69aa3820e2a5f5dc2036ca6b225e07`  
		Last Modified: Wed, 25 Feb 2026 02:03:11 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f3dc6f8d38775beeebfb79a273abcec94dfe4134fc77baab10b8d2c5e38585a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7397831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7edaefc29193c05e39a65b45e1deadeab05cad8b1a36140fe3d82c4d63ee88b7`

```dockerfile
```

-	Layers:
	-	`sha256:b2e6203995b3a82edc25f9ed1f8c924a1f659d7be0220bbc094d3b8b30db41cf`  
		Last Modified: Wed, 25 Feb 2026 02:03:11 GMT  
		Size: 7.4 MB (7382005 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1eedfe2fd7849f2c65fcffaeffb54f5bfc231b9b1c64d41d977ad370cc32a52`  
		Last Modified: Wed, 25 Feb 2026 02:03:10 GMT  
		Size: 15.8 KB (15826 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:d33ef113f1590676f5abcf0bc4bd7e8174aa7405d6daad08f5b31e95769a84ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.7 MB (262739994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:579ede858b8bb10d4c40a93dd0fc5b1393ae98decd403d1e39d49b68b2eab504`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 23:17:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 23:17:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 23:17:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 23:17:05 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 23:17:05 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 23:17:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 23:17:49 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 23:17:51 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 23:17:51 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 23:17:51 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:00b1871f38dea81b1982e306480bd9f97cedf7b0cb3342e4bc84925e6082ade8`  
		Last Modified: Tue, 24 Feb 2026 18:41:26 GMT  
		Size: 47.1 MB (47148087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:965f289f55a9025a1eb0402e10e630cc784a43d5e695e72ee4f0e0d7b8e5189d`  
		Last Modified: Tue, 24 Feb 2026 23:18:26 GMT  
		Size: 135.6 MB (135627060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eaa7a36873d79732ecfeeb3b34dc8aef0225c788964dc667e604a2c44969671`  
		Last Modified: Tue, 24 Feb 2026 23:18:30 GMT  
		Size: 80.0 MB (79963803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:722fa7dc0d320c3dbad194f24a97ecceb5781bb1704beb9fa751a1001d9f710c`  
		Last Modified: Tue, 24 Feb 2026 23:18:29 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872192480e985ec78001fae344d8370e5ca5a38c186ab59b478cc6bd4d7728e3`  
		Last Modified: Tue, 24 Feb 2026 23:18:29 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:0039072db6cea5d93d1093ffaa343b0791dee813404f13caddc99f7aeb0b5701
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7383886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a663b56221e58b7403db6af7bf25370df07262c8f77f7735b0e2abb0e22f55`

```dockerfile
```

-	Layers:
	-	`sha256:6df3338d9abe3fa6e126a77edf978139273cddd01c641d071096cb5b6d973f9e`  
		Last Modified: Tue, 24 Feb 2026 23:18:29 GMT  
		Size: 7.4 MB (7368108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:573b34a2a9f6d3b444e50daf18b553346b338e13ee7194f2fad5db5aa4f619bb`  
		Last Modified: Tue, 24 Feb 2026 23:18:29 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json
