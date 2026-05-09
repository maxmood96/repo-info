## `clojure:temurin-26-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:f0b30c47b9d827bf143a702ee558500223c205c97f147a765376947222d412f8
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

### `clojure:temurin-26-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:181e2d5a5fde4be290b7f861fdcce7f0a8128b54e64441fb94e3531a4dd47492
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.2 MB (196248251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86fa3395205c96887e81b2f6e86f66b14604353c5ea2e7f7870c07fb6295dd13`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:20:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:20:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:20:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:20:40 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:20:40 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:20:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:20:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:20:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:20:58 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:20:58 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7f4310083c0e7fd8146fe30b81bd233a1897232746d35d200a873f6f185019`  
		Last Modified: Fri, 08 May 2026 20:21:20 GMT  
		Size: 94.5 MB (94455692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27d3fef6f22da5eca3673f2426d25277d0b131f0219579a3fae3372cc8b8078d`  
		Last Modified: Fri, 08 May 2026 20:21:20 GMT  
		Size: 72.0 MB (72011292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e45a5f0eddf0a90fc6005e8061b55926de7af871e24bd186118a68cfb63b1d4c`  
		Last Modified: Fri, 08 May 2026 20:21:17 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baba6b9c34ce966e31048115e2f0c030229c24b5a89c30fe426c317e50e1cfaf`  
		Last Modified: Fri, 08 May 2026 20:21:17 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:aa14e63990d0c292d7b42e232a9a9eae0784d752ccf408162dfa23e19cdfe32b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5240501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbad7d7b1e6862e4a39739c3cb46c7dd61f4e26d2941c7de429b3a10328a501b`

```dockerfile
```

-	Layers:
	-	`sha256:b3970a934f540fb1f506ce303dec2f80c2623e45ccda814aab0f4e371f9ca4ed`  
		Last Modified: Fri, 08 May 2026 20:21:17 GMT  
		Size: 5.2 MB (5224696 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ae4beea98f028851ed58e7137d75a5b46caeee066dbd9bf5e39b08cea52fa39`  
		Last Modified: Fri, 08 May 2026 20:21:17 GMT  
		Size: 15.8 KB (15805 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ecb0a40d6b80848bb78054f94e73d1cd0987108c50d1e3f10b7b889c2ac6ab5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.4 MB (195371168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb9ac28f45c4dfd152885f168fde6c20f260472dc2a6f5eb6e51cdb31859071d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:25:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:25:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:25:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:25:13 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:25:13 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:25:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:25:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:25:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:25:32 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:25:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf0593f752e502b65034a0c80cac7ef6bc6dc3c342a4055c2f6c8f35d2b8554`  
		Last Modified: Fri, 08 May 2026 20:25:54 GMT  
		Size: 93.4 MB (93395168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5a3ad3146388fb91b63a3b253c5c62a885ce5657baddda9c501e633aae62a1`  
		Last Modified: Fri, 08 May 2026 20:25:53 GMT  
		Size: 71.8 MB (71831316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd39f96b9671e631a40137c702cc9ea3f1eab1125c207d52352bb1a50ec22e7c`  
		Last Modified: Fri, 08 May 2026 20:25:50 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87c059eadd079e18add97b8e6a085eebc1e174c540fc060b6921d179fbb31a0`  
		Last Modified: Fri, 08 May 2026 20:25:50 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:dff548ac9136da0a55e13f508b3d0fee1ce958ef7b441635bb53aaac048fb79b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5246385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32ae99d19b22a0c366c0ea192540d4595bea6cbe9f5247c90381c5de5bd6b965`

```dockerfile
```

-	Layers:
	-	`sha256:ee51e6d84996c57e5fb9fd1e86bebadad427518b5f1b83005ab0a6665c6b3748`  
		Last Modified: Fri, 08 May 2026 20:25:50 GMT  
		Size: 5.2 MB (5230462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fc26ee1a7c576d6d2baefb149cb0dbe0be59a480dbed7d1fbc0fc1382c564b2`  
		Last Modified: Fri, 08 May 2026 20:25:50 GMT  
		Size: 15.9 KB (15923 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:0f7a9ac083fd432984122ff61848aaf5bde2040b9be1ac096195348485306896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.8 MB (204809251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efb6cd2f29d90860cb531cdbe2161270baecb8d14312fcefdd460616a6d83803`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 08:52:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 08:52:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 08:52:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 08:52:30 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 08:52:31 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 08:56:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 08:56:16 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 08:56:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 08:56:17 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 08:56:17 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b5fd051d0fcd0789e7358cba300f83befdba943416041497be86050e282a6d02`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 33.6 MB (33598032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e771730505306c65b920a33ea03d87b316b140e1fe4d13ec6a98c1278d920c3a`  
		Last Modified: Wed, 22 Apr 2026 08:53:41 GMT  
		Size: 93.8 MB (93781494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8373c0f62241966237311cf27655f2ffa5199dbd7f2b2d461d2324a1dbcbea6`  
		Last Modified: Wed, 22 Apr 2026 08:56:53 GMT  
		Size: 77.4 MB (77428690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7706d05826018f9c78aefbc6befd5bb6ac4d821243baa99f5ea4ef66605c6b59`  
		Last Modified: Wed, 22 Apr 2026 08:56:51 GMT  
		Size: 609.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4315b1e98556f8f666fc098c3224bfd8fbeae9d8859288ac55906013515b2369`  
		Last Modified: Wed, 22 Apr 2026 08:56:51 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fff36e7e596901befd404c1dea8964fc323bb5a29cf8385369fb5a0b6764814e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5228856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e8643e214e7550c608e0751ecc19b3555084b15bd2f44a5928b873427ba9ba0`

```dockerfile
```

-	Layers:
	-	`sha256:9d397371c2603a53e7f38d9820954f168f15328a325dd777e14d8671ef869ef3`  
		Last Modified: Wed, 22 Apr 2026 08:56:51 GMT  
		Size: 5.2 MB (5213003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b35ff088a8d0af786a096f98e41a4f7dd36ac6b5ef5e5efcdd06e6bd932364d`  
		Last Modified: Wed, 22 Apr 2026 08:56:50 GMT  
		Size: 15.9 KB (15853 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:7af8afea9d39b5764273c0a4b76ea23b57d4d1bd3477538633fae698be0da22d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.2 MB (192190233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e469c060b1f789c59c59ed6c42326aec9dfef498f24940ef3ff2afe4132686d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Fri, 24 Apr 2026 19:10:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 24 Apr 2026 19:10:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 24 Apr 2026 19:10:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Apr 2026 19:10:34 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 24 Apr 2026 19:10:34 GMT
WORKDIR /tmp
# Fri, 24 Apr 2026 19:26:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 24 Apr 2026 19:26:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 24 Apr 2026 19:26:38 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 24 Apr 2026 19:26:38 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 24 Apr 2026 19:26:38 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4570a2040f6cfb5fdde4314c204e28e913195fc06cfb70d3ed0994fb7a93519a`  
		Last Modified: Fri, 24 Apr 2026 19:15:57 GMT  
		Size: 93.0 MB (93008135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d7aafa3a88c354e3b14e67e21485b3b14ecf5b7b6794eadadd0c183d4fa060`  
		Last Modified: Fri, 24 Apr 2026 19:30:09 GMT  
		Size: 70.9 MB (70900863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4175bf8f566a106c56f244fda6edcf5b86f897f2b9bd6f1b5afa415b11a1958`  
		Last Modified: Fri, 24 Apr 2026 19:29:58 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77da22c728253cf1215f5d727d3734f7d8f4809521153d3ce10060548cd8fb19`  
		Last Modified: Fri, 24 Apr 2026 19:29:58 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1b9010f629abd5995ca1e95f3c950de339928c02086ca37543f5294cad3ff064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5212648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f230dec7ad72de068275f499e022759b2f4cfe53c1d627fbd4a4b8bf1be026d`

```dockerfile
```

-	Layers:
	-	`sha256:d265cf604a10fa167a3c0bafea61c3bab16da1dddb245ebddb744e9f3d457b69`  
		Last Modified: Fri, 24 Apr 2026 19:29:59 GMT  
		Size: 5.2 MB (5196795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6e4b428660b4bf2a272b43f115f991a0407321b4d98d7f4c1b9189d831f0a43`  
		Last Modified: Fri, 24 Apr 2026 19:29:58 GMT  
		Size: 15.9 KB (15853 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:ee4b662c5ecae8ba01596520f2b1e077b8423cfe040a9db11814d8559d6757f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.4 MB (193376251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc2c554f221a7e4c15b319a62146e92335f90bd3ac47ec766df0ff207b86ea50`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 22:21:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 22:21:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 22:21:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 22:21:40 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 22:21:40 GMT
WORKDIR /tmp
# Fri, 08 May 2026 22:22:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 22:22:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 22:22:56 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 22:22:56 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 22:22:56 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2fbbc68c452b3ba3a496488f38159dac53afe693311bee1c04f555d854ff4a2e`  
		Last Modified: Fri, 08 May 2026 18:29:20 GMT  
		Size: 29.8 MB (29840347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3817b208f05ee63b0a9ce8a4a4cea90fec7bb6bb641467a82d11ac5bde2fac`  
		Last Modified: Fri, 08 May 2026 22:22:19 GMT  
		Size: 90.5 MB (90547679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e492b9d1c35a8b34ca5c5601f8a2e5f0a6813d22585e3e2b1b740a4b5e3809`  
		Last Modified: Fri, 08 May 2026 22:23:21 GMT  
		Size: 73.0 MB (72987187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:416ac3cdeaef85b201ae9ec6fbba9b162d570c71b845fd31f355742022369954`  
		Last Modified: Fri, 08 May 2026 22:23:20 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfbfe490086ed742627b27f6cafa2052cc66c667ba2b851ef92f2a444985581`  
		Last Modified: Fri, 08 May 2026 22:23:20 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3aa8d97f0e75f79c187da58b1a7691c0d3d24f00110a953ac873c9f7ae68fe9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5221611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86e28b6e8031e0f5f12f045519bdd6f44e386318bf2fd189b106b6eda738a1bb`

```dockerfile
```

-	Layers:
	-	`sha256:51e93a8ccb2be275ebc1a87e6c616c3bb5f0d6bdc77c818ca4e20670d6c516d2`  
		Last Modified: Fri, 08 May 2026 22:23:20 GMT  
		Size: 5.2 MB (5205806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91fb71c8a77546c3369be7103cc2059c4e75a596f42160d4f52174e55b2696bb`  
		Last Modified: Fri, 08 May 2026 22:23:19 GMT  
		Size: 15.8 KB (15805 bytes)  
		MIME: application/vnd.in-toto+json
