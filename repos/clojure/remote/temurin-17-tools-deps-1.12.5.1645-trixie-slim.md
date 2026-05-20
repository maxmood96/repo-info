## `clojure:temurin-17-tools-deps-1.12.5.1645-trixie-slim`

```console
$ docker pull clojure@sha256:ebaaea0786e76c33c1862a00b5367b17cca4c0d3edd0dc4a4d78d945c70929af
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

### `clojure:temurin-17-tools-deps-1.12.5.1645-trixie-slim` - linux; amd64

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

### `clojure:temurin-17-tools-deps-1.12.5.1645-trixie-slim` - unknown; unknown

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

### `clojure:temurin-17-tools-deps-1.12.5.1645-trixie-slim` - linux; arm64 variant v8

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

### `clojure:temurin-17-tools-deps-1.12.5.1645-trixie-slim` - unknown; unknown

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

### `clojure:temurin-17-tools-deps-1.12.5.1645-trixie-slim` - linux; ppc64le

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

### `clojure:temurin-17-tools-deps-1.12.5.1645-trixie-slim` - unknown; unknown

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

### `clojure:temurin-17-tools-deps-1.12.5.1645-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:b1aeca3f39701dde213fad7e08701bb4b11afa1fe928ef2cb6d2b853aff3473e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.8 MB (238767522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0bc39017035bb491a40af35b27ad4b815434abc44d391da667e2749f718c704`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Thu, 14 May 2026 23:35:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:35:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:35:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:35:32 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Thu, 14 May 2026 23:35:32 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:26:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:26:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:26:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:26:46 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:26:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2fbbc68c452b3ba3a496488f38159dac53afe693311bee1c04f555d854ff4a2e`  
		Last Modified: Fri, 08 May 2026 18:29:20 GMT  
		Size: 29.8 MB (29840347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeabeb56e1eebe9b1edc136c9b084b501f34255e33a2b2c7f5f66dcb37c977db`  
		Last Modified: Thu, 14 May 2026 23:36:20 GMT  
		Size: 135.9 MB (135910407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54542e054e95f3a328878dcd5cba018694dc4e323712549ce58762ef87e1fe5c`  
		Last Modified: Fri, 15 May 2026 20:28:04 GMT  
		Size: 73.0 MB (73015724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91eaf3c339079d392fdbe4d6ceee0d9b511cd477491ecfb893b654c501f9e277`  
		Last Modified: Fri, 15 May 2026 20:27:59 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50d8d03ed0f7295d58e7567b92b0a052665b39d97b9e693d01dd214eaee360a`  
		Last Modified: Fri, 15 May 2026 20:27:59 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.5.1645-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f529d1a519eaa3f64aeceddf581b3ba3f5f4fbcdbe51cb234997f782db4e8468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5270788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:065bc67e6754187f807e8e53a793caac972641054450cfa9b09fc13d4472ae6f`

```dockerfile
```

-	Layers:
	-	`sha256:698ee9ed3f7f74bb3b440fc9bdb344a92b53dff4195c79b270395af84b60c48d`  
		Last Modified: Fri, 15 May 2026 20:28:01 GMT  
		Size: 5.3 MB (5255777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e70454192b6a3fa8c8ff3db67936a9687f17126f3f56603a600ff723672fbbd8`  
		Last Modified: Fri, 15 May 2026 20:27:59 GMT  
		Size: 15.0 KB (15011 bytes)  
		MIME: application/vnd.in-toto+json
