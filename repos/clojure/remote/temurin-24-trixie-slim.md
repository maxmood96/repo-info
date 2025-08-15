## `clojure:temurin-24-trixie-slim`

```console
$ docker pull clojure@sha256:daaa0134aece5f03a07ac9c6eb1f9af34470fa60fc7eed81086960239745cc3a
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

### `clojure:temurin-24-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e8cc38607ae3ee6d06570d721e6dfd1afc41dbd5f9080b499207c1546ebb1eed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.6 MB (191590066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efb18165c2da45b79000db60222e5fb3012fa0586d89f66ea23544d6884bb4f1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
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
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e087d8cf453ee14a84122c366da6cb37eab6d898c9aa9a5a4d357be9c121c5ee`  
		Last Modified: Tue, 12 Aug 2025 22:36:10 GMT  
		Size: 90.0 MB (89975231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c813543e64510412f7d7c214f4500546e757905b9fc8516980be7af1eb338ea9`  
		Last Modified: Tue, 12 Aug 2025 22:40:35 GMT  
		Size: 71.8 MB (71840509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3d0f95894d435ff3cc4954a4e7e8f604d8c3f96010d2efd3a04df90b7cc6be`  
		Last Modified: Tue, 12 Aug 2025 22:40:31 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5803bb5711d1f353388711cdddf359cf844591508717e1bead82eafc97b367`  
		Last Modified: Tue, 12 Aug 2025 22:40:32 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ee1394868114b5132a800e83feee300b01a5421138b1c5f452735dcacc4fe8a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5221704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2116b93a5d7f412161f92e2d7bdf0ee1532d73ed7b11351bdfb3ed441aa4451`

```dockerfile
```

-	Layers:
	-	`sha256:a6118914b32835c2085b458dce86160308644be15c71db10c1db660a90024b9b`  
		Last Modified: Wed, 13 Aug 2025 00:41:11 GMT  
		Size: 5.2 MB (5205856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd8d98f63f0669e209d27827bbeee64990ede42a9eea8c7255b2631fd2cd6e69`  
		Last Modified: Wed, 13 Aug 2025 00:41:12 GMT  
		Size: 15.8 KB (15848 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:cd022291d16df85072e55981a448c8080803f7d0e3863b4b59d6453aefe2ba47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.9 MB (190893121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1d54868b13cbc709f1cecc4d79b53b61135432d12b16b5575267572f5b2d527`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
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
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8928066aa1cffde6052473d0487eb9a4df6a536628d5688407e0706fb92f50f`  
		Last Modified: Wed, 13 Aug 2025 14:44:57 GMT  
		Size: 89.1 MB (89092517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d416c0c337e72c9891a75454b1e4c3dce572089eece7f795d069ca2d6ff6ddf2`  
		Last Modified: Wed, 13 Aug 2025 14:50:29 GMT  
		Size: 71.7 MB (71663520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d1560ba0a8f2b34fca8b291a48620ec042fba0e145f69b88612549a8cb51fe`  
		Last Modified: Wed, 13 Aug 2025 14:50:03 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9548a101d43e2adb4027d0151737804874809b082b20dcc4a3647b11312ec9f1`  
		Last Modified: Thu, 14 Aug 2025 09:39:08 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d0385eae019145bc8ab1080c4c08105969616382a5193726096f97c04787dbf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5227587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1aef8c366dcae62b196d51522dcdae9fd861e899c66f1c51de59cea39fbefca`

```dockerfile
```

-	Layers:
	-	`sha256:d9f7be1aa30593279249f07ac4caf558823e4cd1f34c9190e8c5579225e74adf`  
		Last Modified: Wed, 13 Aug 2025 15:41:47 GMT  
		Size: 5.2 MB (5211622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b4df960527b42d443e33078154950182fa5e2b3178d984d065b883388a7223c`  
		Last Modified: Wed, 13 Aug 2025 15:41:48 GMT  
		Size: 16.0 KB (15965 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:3d9e539c70a367c6c46f145d2d2104e0916b9cd0a93761ea368b41587ee49758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.8 MB (200760258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19c3e10270c3e237daf3223c38ce7251a4a8e19f27633c59735b139b266508ae`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
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
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e503be160eb21d6debdd1af37b0b1d7078c455d27a1cc4aa48952b550f16291d`  
		Last Modified: Wed, 13 Aug 2025 20:24:59 GMT  
		Size: 89.9 MB (89918237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f51b0e459782d2ad1e3159ed3196254e5994356986daf777d0e35aca6a6399`  
		Last Modified: Wed, 13 Aug 2025 20:32:27 GMT  
		Size: 77.2 MB (77246764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f025ca41ed90c565b92754a920a1c35b4489e5039140a132426f9039f47560`  
		Last Modified: Wed, 13 Aug 2025 20:32:06 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b01e603886c427a190a9077eff1d57e139e9a7e9db19f42ace80993a843ce523`  
		Last Modified: Wed, 13 Aug 2025 20:32:06 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1b5b95254f794dd295cb709fb44606338fc6bccf282f872582c8489ca5542dcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5227421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5462ac8b71aad917e8e88f8721554a664ece6286730786a608337eb41ddb6cd5`

```dockerfile
```

-	Layers:
	-	`sha256:5608c4ee81f94a2fcbfbf9ed4e11447c63bfbb42ef459e81cf7398ceb30ff929`  
		Last Modified: Wed, 13 Aug 2025 21:40:03 GMT  
		Size: 5.2 MB (5211525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5c0756d40678e3494ad3b8d14952c1b6d3d2d1de52b13213571b772faa3b3be`  
		Last Modified: Wed, 13 Aug 2025 21:40:04 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:300eea5da186f420dd86cbaeb411f0b7b086729952dd12cdcf6de1a0596ad024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.7 MB (186674475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f5b9f1d685aaef323b9e695f02014a4648e7854f5bb7f2b596dd10c3bbd3c91`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
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
	-	`sha256:a37386b9234ad75f65b5aa72f3d919ff0eb3bb18978566fa959d6e357480594c`  
		Last Modified: Wed, 13 Aug 2025 04:01:43 GMT  
		Size: 28.3 MB (28271623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97125372afb3e2f47113a36e62b460f48c50f45d3384089379e7fcbef7e6354a`  
		Last Modified: Fri, 15 Aug 2025 08:12:50 GMT  
		Size: 87.7 MB (87670395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:121c6abdb7d0081be9168deb88d9e2c792ad68fadeb8d691d241c3a27335db75`  
		Last Modified: Fri, 15 Aug 2025 08:26:36 GMT  
		Size: 70.7 MB (70731415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9e2c85cb2282341472b751b49e75057802ca88a97552270796bedc66e6c4cf`  
		Last Modified: Fri, 15 Aug 2025 08:26:32 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811a0aa8afbe735914053a379fd78204dc9c5067d02f2cfc22eca66c9a5d6757`  
		Last Modified: Fri, 15 Aug 2025 08:26:31 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5323313d2acd89501cd0a94755ee75b2d186be3ad6f12841b95ed3a7fe810875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5211213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42331ed48e9ab896e01d5aabe7195c742b571c207ad61f0a2365f869b40e6c97`

```dockerfile
```

-	Layers:
	-	`sha256:448cca53ba06a8bf09e13492b740bd434f0f31ae8287feee019daf5d63b2e51e`  
		Last Modified: Fri, 15 Aug 2025 09:37:47 GMT  
		Size: 5.2 MB (5195317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5f5bfdf001966cd532c7c6138400dccfa8d61c518e8eee08639cba9cf4752d2`  
		Last Modified: Fri, 15 Aug 2025 09:37:48 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:4ab2012b69e9277ed781e0bdb9b90ff45ce23a18290153d778aff84002dcc292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.9 MB (187865115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9bfd871c2184cbbcb73c48819102881a92219688b4323996bd40f430b12da70`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
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
	-	`sha256:bfe4d60a27c9392ab729f16b50a763cda36622d744066c3cf029a072133f2907`  
		Last Modified: Tue, 12 Aug 2025 20:59:52 GMT  
		Size: 29.8 MB (29833057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3190129e531a7f25747cd871a43c407ee1e089315aadaf3bce7c587df21a3117`  
		Last Modified: Wed, 13 Aug 2025 07:29:02 GMT  
		Size: 85.2 MB (85226398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cbc6daa06a6c33c85321abf0df64336a9d9b449ee3f523ea7008dcacb4b66da`  
		Last Modified: Wed, 13 Aug 2025 07:31:24 GMT  
		Size: 72.8 MB (72804618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d20b106355e771072f62268620ab718fed5d11e295b40f8e6103a702dbe3c9`  
		Last Modified: Thu, 14 Aug 2025 17:51:18 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:308ec94b2f5da0e50bdeb5f4a4303b77d25846b3e187ee7af811bd44785f924d`  
		Last Modified: Thu, 14 Aug 2025 17:39:19 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8ad265d648f4bbc8d2e11ce22ec0588940a31183b48979a4c05aa94980686f74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5220176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c370fc28050c5a433c11de62cd8be4b64c5fd59e356441c0469ab44b5d0307d3`

```dockerfile
```

-	Layers:
	-	`sha256:d312beee0110f6ae159fcb06a2aebc0131c0257ad7e121a0d18ead65ef595471`  
		Last Modified: Wed, 13 Aug 2025 09:39:15 GMT  
		Size: 5.2 MB (5204328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d0821b28f33f36693befae16180accce9a5ccd9d8c9f05db7954694ea696fc9`  
		Last Modified: Wed, 13 Aug 2025 09:39:16 GMT  
		Size: 15.8 KB (15848 bytes)  
		MIME: application/vnd.in-toto+json
