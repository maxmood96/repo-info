## `clojure:temurin-17-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:5a8df1705f78360fed9207a4a35bd6214d7bedd607092d825f817406ac89e8c9
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

### `clojure:temurin-17-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7c53554600609262b2d4077745a2a18c3cd0b339f5ff616497bbbc3b6d8db049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.7 MB (247733680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e38dce19a3fc19dcfc2e7a48c5248376008d404d7041b00e49ec3f622f7641d3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:59:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 May 2026 23:59:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 19 May 2026 23:59:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:59:20 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Tue, 19 May 2026 23:59:20 GMT
WORKDIR /tmp
# Tue, 19 May 2026 23:59:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 19 May 2026 23:59:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 19 May 2026 23:59:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 19 May 2026 23:59:34 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 19 May 2026 23:59:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f672bcd8117080a1ecfdee68a637dfa3ebde1155dbfc92ad9e6b2a268c0f4a6`  
		Last Modified: Tue, 19 May 2026 23:59:55 GMT  
		Size: 145.9 MB (145905454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df44429d21985a9357c3f671900ff0e73d133541b543ba07edf76f3720e1d25`  
		Last Modified: Tue, 19 May 2026 23:59:54 GMT  
		Size: 72.0 MB (72047261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f2b8a926d3f0717f0047eb2d18ec836c5c53609446347351cb0a6f3f6245569`  
		Last Modified: Tue, 19 May 2026 23:59:51 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0878e0fdaf4282b5a284606905ce48aa982eda0e041f5f5ed1107f96037b409a`  
		Last Modified: Tue, 19 May 2026 23:59:51 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:957983c1f2e6d0a580c4341d31f0ff5d32e344c88c5cd19d17e0a10b51b8e8c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b418b6d1620d09b2b5ba7cda9ff083a4097429e48082ad93af7fdcaaf2c97736`

```dockerfile
```

-	Layers:
	-	`sha256:d82cfad08f22173acc0764f905336522cacd675e7ea83f25c78dece405002c55`  
		Last Modified: Tue, 19 May 2026 23:59:51 GMT  
		Size: 5.3 MB (5259967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c156cb4d0a04b534142a79561a04eaf7b1816a45d486328c035f3bfb6090a233`  
		Last Modified: Tue, 19 May 2026 23:59:50 GMT  
		Size: 16.0 KB (15966 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:44e650710edd67ebae154a3852d0d58e5a546ed2a4526ecfb80b69cdee9f56dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.7 MB (246738574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:007f56aa0c79cd52a46e97637510933b525862c49ffb9ce4d4cb2b9353897df0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:06:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:06:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:06:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:06:12 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 00:06:12 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:06:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 00:06:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 00:06:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:06:28 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:06:28 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:934929ff9f16f89563fafd9fac6adc194b6543d7e750222b702c18d8be093859`  
		Last Modified: Wed, 20 May 2026 00:06:50 GMT  
		Size: 144.7 MB (144724336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:602a0639ff68f660c034c82a90464c52b2b7024fb806155fcf92beddc12781a2`  
		Last Modified: Wed, 20 May 2026 00:06:48 GMT  
		Size: 71.9 MB (71871277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8b9f5985a112e530ffb8f26cf56e7040b280d48c86e9445abd28bb6470d54d1`  
		Last Modified: Wed, 20 May 2026 00:06:45 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c01ad3c09e20a0cc56e8ac78f993efc06c19ba17483618a366e687af2da09d6`  
		Last Modified: Wed, 20 May 2026 00:06:46 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bcedc412c9ca9a3aa83648ef18f32f33513a54d23c4bcf4771a29a5a5169dab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5281812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f70d6848f3c3cbc22816b0968719e4ec07262a255d705879a66bd794e21902a8`

```dockerfile
```

-	Layers:
	-	`sha256:828c1bf64901a1bcc01a0b910fe0cf614baea12f4a74908c94e0e226437e9e69`  
		Last Modified: Wed, 20 May 2026 00:06:46 GMT  
		Size: 5.3 MB (5265728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a970b5fbb324ad2ffda5934295f3f7c4491fa054704e0bb96aa9437eebccc16`  
		Last Modified: Wed, 20 May 2026 00:06:45 GMT  
		Size: 16.1 KB (16084 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:f3b02f957c37fbc1fa242dd736835cb20520ff22be847b848f297dbf36409a70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.8 MB (256821439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea8d46824ec2fe914a9a0809d4c66db4b66d0ebaa2ab004be8b4fb57542bb387`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Sat, 09 May 2026 02:32:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:32:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:32:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:32:03 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Sat, 09 May 2026 02:32:03 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:26:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:26:31 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:26:31 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:26:31 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:26:31 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b9baa45d89920bd180d7551ccc5bc535e0c5f55b863ddebddfdc06f9436dfe91`  
		Last Modified: Fri, 08 May 2026 19:46:53 GMT  
		Size: 33.6 MB (33598087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f72cabc9601635085bc11fa48d74114d9e1765a07685bad636cd3a7da9370ac`  
		Last Modified: Sat, 09 May 2026 02:33:09 GMT  
		Size: 145.8 MB (145766215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a6e1403bb0602ad9dd6c3cd7be974b170038472916b67f7728e6a212bb19cd`  
		Last Modified: Fri, 15 May 2026 20:27:07 GMT  
		Size: 77.5 MB (77456095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976fa490c8c4e2ffd8b959c58c086e64132d722f43d74a86eecd0cb66f45ad5d`  
		Last Modified: Fri, 15 May 2026 20:27:04 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5460bc3a0f4833eebbcc937e1377815a22b3c099b545c61b96ea1a2b68318ce`  
		Last Modified: Fri, 15 May 2026 20:27:04 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ce9311fe925d367f6e4dea3e04031cc96411432599d1de97229a93e55779eb90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5279283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91dd7ddab9ab84a62be92a8e2b709f9633670430b7d656467b2acff0a0601925`

```dockerfile
```

-	Layers:
	-	`sha256:4bc491786ea639ee44ee9978e9a4b93d5f7c81c6189dee72e0723ba05b9121bb`  
		Last Modified: Fri, 15 May 2026 20:27:04 GMT  
		Size: 5.3 MB (5264224 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fa24eaad8a5c8ce03e69dbff106bf08e4df55fe0a0c1da34ca5a0f9391236fb`  
		Last Modified: Fri, 15 May 2026 20:27:04 GMT  
		Size: 15.1 KB (15059 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:3bbeec5ce24e3252df88022c441a289f0cef26ec05341ae65ca9db1b2aedac41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.8 MB (238786228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adb607e74d0bfead3ef817f605342c2e2ab0322951b7e8d9dcfaf241af7091e0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 01:44:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 01:44:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 01:44:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 01:44:03 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 01:44:03 GMT
WORKDIR /tmp
# Wed, 20 May 2026 01:45:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 01:45:17 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 01:45:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 01:45:17 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 01:45:17 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3a7bf300ab749fc8aaa5ec872160f889b9f1fd11db31bb5e8fe4d9ec131347b0`  
		Last Modified: Tue, 19 May 2026 22:36:59 GMT  
		Size: 29.8 MB (29845924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b7061a0b137c526c9908a364ab29b9c6acb42a84835c646b8c4d2dde37fd77`  
		Last Modified: Wed, 20 May 2026 01:44:44 GMT  
		Size: 135.9 MB (135910410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec6213aaa4a311e7901073aec7ac79fca93e01f7a908b9aef1a8e2b33b849ac5`  
		Last Modified: Wed, 20 May 2026 01:45:41 GMT  
		Size: 73.0 MB (73028859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73a3f00969346b0793b41d3c29c64f5b89304cf0d3ea364bf26277391d738d01`  
		Last Modified: Wed, 20 May 2026 01:45:39 GMT  
		Size: 609.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd6fb70362a0002326e61185c437ce596fbd83fb8429ec39e7a2c9616729f57`  
		Last Modified: Wed, 20 May 2026 01:45:39 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0a81be625f1cabd671eab42844e5fd21e286a9f5b65120028c6128f668d7d74b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5271857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac31a6086f1e5a99827f06cb435f617f04dbbb42000b2a6cb5031dd3e42b806c`

```dockerfile
```

-	Layers:
	-	`sha256:bc4a7dc0557c7fff5472444f130a35f17b4c4015e636b575e1017353dd4428f9`  
		Last Modified: Wed, 20 May 2026 01:45:40 GMT  
		Size: 5.3 MB (5255891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dfe50e58c50c3cc9faab196f85fb796dc33ff2deb8105bb311aaccfcce8da78`  
		Last Modified: Wed, 20 May 2026 01:45:39 GMT  
		Size: 16.0 KB (15966 bytes)  
		MIME: application/vnd.in-toto+json
