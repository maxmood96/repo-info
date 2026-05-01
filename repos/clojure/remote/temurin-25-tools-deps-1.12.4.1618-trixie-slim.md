## `clojure:temurin-25-tools-deps-1.12.4.1618-trixie-slim`

```console
$ docker pull clojure@sha256:1b1eca237fc3a5225b0400ee85b99fb7acd60db86a8840e623e78933ddcd50bf
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

### `clojure:temurin-25-tools-deps-1.12.4.1618-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:639dabd3ed5cf2637b64e5b84d24afaa16640c9d70747d369f037396a39d10e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.4 MB (194367048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f55804a9eb7a21c77e7418db886a1eac7d0befe6d43f2182de7879bfdc4941c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Thu, 30 Apr 2026 23:53:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:53:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 30 Apr 2026 23:53:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:53:38 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 30 Apr 2026 23:53:39 GMT
WORKDIR /tmp
# Thu, 30 Apr 2026 23:53:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 30 Apr 2026 23:53:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 30 Apr 2026 23:53:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 30 Apr 2026 23:53:55 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 30 Apr 2026 23:53:55 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5a8ea7487e8e93593194422f890238ef37242057ee08bfbd80ce371fb01f67`  
		Last Modified: Thu, 30 Apr 2026 23:54:16 GMT  
		Size: 92.6 MB (92574598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f790efb308578aba2c893a38331c9477781aadc4617283e9864c931ce04f9caf`  
		Last Modified: Thu, 30 Apr 2026 23:54:16 GMT  
		Size: 72.0 MB (72011235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b04093f8649375c6fd7f4778cef890090142aef9f0a7a56d0153a8ae8e1d9d`  
		Last Modified: Thu, 30 Apr 2026 23:54:13 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7697312d520758eefb408641e476d495b6b5659ef05329e0d9913210e914723`  
		Last Modified: Thu, 30 Apr 2026 23:54:13 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1e7e4332559511bd4c095e13667c4b1ceb332de26ff4c060d3423e0d21e56ae1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5244394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55eb1741b8c10ba8517153b38c7fa805e7066a6051c2b16052ce1af07b6de881`

```dockerfile
```

-	Layers:
	-	`sha256:ba68c64e48eb7db84bdbcc4ef343e7a6c71c565588c76d46c0d8c0be0781c187`  
		Last Modified: Thu, 30 Apr 2026 23:54:13 GMT  
		Size: 5.2 MB (5227901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ad5dbfc8bd50ee89d332677ec192898c92a18a834a8e4dd3a4bbf6b6e3b96ef`  
		Last Modified: Thu, 30 Apr 2026 23:54:12 GMT  
		Size: 16.5 KB (16493 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1618-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d07cf7fba65c218275ec3c71a93a07c6a55efe40f8aaba3fe15c978887158a73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.5 MB (193518511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8170b06f9c58bda9718db259c6be4888192101094d2a736ea97df115e5f513e7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Thu, 30 Apr 2026 23:53:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:53:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 30 Apr 2026 23:53:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:53:21 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 30 Apr 2026 23:53:21 GMT
WORKDIR /tmp
# Thu, 30 Apr 2026 23:53:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 30 Apr 2026 23:53:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 30 Apr 2026 23:53:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 30 Apr 2026 23:53:39 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 30 Apr 2026 23:53:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095815c5f94b82efe420057840d44ba0b7296e0a37626de3e5dfbdffe7cd7b7c`  
		Last Modified: Thu, 30 Apr 2026 23:54:02 GMT  
		Size: 91.5 MB (91542287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d8802b0010e42995714d9804c96ed3b3153b1a20d0562a1fe1c732b90ef6ab`  
		Last Modified: Thu, 30 Apr 2026 23:54:02 GMT  
		Size: 71.8 MB (71831577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a250c4b1e6e7016a6c342c076a130b959a649eefa7683e3256510ff16000cd2`  
		Last Modified: Thu, 30 Apr 2026 23:53:58 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1601ae0ae46142957405ce541386184ad359c09d54788777686a19c74513e6e`  
		Last Modified: Thu, 30 Apr 2026 23:53:58 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b3b81aad0b745421ff450ac675a98a2457df5e602a65de0c55bc723d32ed83d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5250326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb50af84ca54f14727ec3965be2d0224d3ffeafdcab2be6145b413afbcdf79b3`

```dockerfile
```

-	Layers:
	-	`sha256:53442a20ac84e1f7ad46008791ecd2ca463e2476dea4e33c172cd6e51fc04913`  
		Last Modified: Thu, 30 Apr 2026 23:53:58 GMT  
		Size: 5.2 MB (5233691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2fca54f2e72a185b03c9f54c3850779b18514193da02fa625194eafacf6c57a`  
		Last Modified: Thu, 30 Apr 2026 23:53:58 GMT  
		Size: 16.6 KB (16635 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1618-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:7b8579de83dd38029051a2a7f387d07866be171a5ba06ef42493ac5ab0d81e1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.9 MB (202942094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74f31fab5a46a2ea1fcb15563886da96f65ccdd576d6ff63f52f8df69dd11f2c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Fri, 01 May 2026 00:10:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 May 2026 00:10:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 01 May 2026 00:10:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 May 2026 00:10:37 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 01 May 2026 00:10:37 GMT
WORKDIR /tmp
# Fri, 01 May 2026 00:16:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 01 May 2026 00:16:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 01 May 2026 00:16:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 01 May 2026 00:16:41 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 01 May 2026 00:16:41 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b5fd051d0fcd0789e7358cba300f83befdba943416041497be86050e282a6d02`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 33.6 MB (33598032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec707715d5c468147a426fc06e8d344ac9ef674c52a229b56d8aeebfbce15f60`  
		Last Modified: Fri, 01 May 2026 00:11:56 GMT  
		Size: 91.9 MB (91914033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:048d6390bb5f94a63cb50f9db9c99d866bb0a236909982bb83ca2cd3a65baf3f`  
		Last Modified: Fri, 01 May 2026 00:17:31 GMT  
		Size: 77.4 MB (77428991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6fb5bfbb057752cadf82005e6f60146b12c9262c1fa29d5bf338ea5185916a`  
		Last Modified: Fri, 01 May 2026 00:17:29 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86056507873fefc348d32cac0a695465ead062c766dff0107db605380c69298f`  
		Last Modified: Fri, 01 May 2026 00:17:29 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:729ea65a2a12dfa99667c4480d652e9c8138f5e8a26087f30f391489e0741e95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5232149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dfc8a50e6e43d4d2ad8632f789731423efa1331e2efb3ebee8d37298929fca2`

```dockerfile
```

-	Layers:
	-	`sha256:79ac7901ac0cca093a9138d3232f6f171f16ea683d37d26061387e0490a5d5ac`  
		Last Modified: Fri, 01 May 2026 00:17:29 GMT  
		Size: 5.2 MB (5215596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63bb45cc7d69ef17a13b0f5229480a35671a4c9c0796adb835fc7b33fc960449`  
		Last Modified: Fri, 01 May 2026 00:17:29 GMT  
		Size: 16.6 KB (16553 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1618-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:be89d0af9b54d14061ba4963cf632c0abdeebf260743bbc63cf55dc9852cfa3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.2 MB (190196910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fa21e97ea281844cdcea1fbc02f616d0e17dcda82be06e225d98d1fcc0e91bc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Fri, 01 May 2026 01:17:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 May 2026 01:17:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 01 May 2026 01:17:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 May 2026 01:17:25 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 01 May 2026 01:17:25 GMT
WORKDIR /tmp
# Fri, 01 May 2026 01:40:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 01 May 2026 01:40:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 01 May 2026 01:40:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 01 May 2026 01:40:01 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 01 May 2026 01:40:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a463537893b115e8f6bf5847dfb28b93d1015ffeaba8f0acf52e10133dfcf3`  
		Last Modified: Fri, 01 May 2026 01:22:48 GMT  
		Size: 91.0 MB (91014937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189637ec0b992e6712b62b6fb4f7b70346d8d5bcb3ee094fd4aab889fff4c37f`  
		Last Modified: Fri, 01 May 2026 01:43:39 GMT  
		Size: 70.9 MB (70900737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79eaea740b68965c8fdc3649064b2c913832c335f630b9ba2a8384fb8106320d`  
		Last Modified: Fri, 01 May 2026 01:43:28 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e977049073a11f7f44c386d34f63afc5a55ee22fb7bc04268acd8cc3aca264`  
		Last Modified: Fri, 01 May 2026 01:43:28 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e91e0fd693ca996b99de0cbe7c0cd9858b0a648a250235e9c08fd4549071b198
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5215940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a6965907ae999b8e0337c662e8c9772925e92bfc1a659806cc6fa700e443fec`

```dockerfile
```

-	Layers:
	-	`sha256:cbd087a5706682fae7db02ce8143c7d1f9e49a1a746c6749c8ab1d763063d0f0`  
		Last Modified: Fri, 01 May 2026 01:43:29 GMT  
		Size: 5.2 MB (5199388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b976013de3d9592c571721b84f129ce8eee150012ccf55a24491e0511d7c0ff9`  
		Last Modified: Fri, 01 May 2026 01:43:28 GMT  
		Size: 16.6 KB (16552 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1618-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:f914deb7f8b28b0801f0a57d3d408a4750d25f5541c1364e59fcafbefa887546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.2 MB (191248936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:308b9018ea73962501cda5455ba58a51f551c9b093f031c8e0a49d0f02c3a835`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Thu, 30 Apr 2026 23:50:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:50:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 30 Apr 2026 23:50:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:50:52 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 30 Apr 2026 23:50:52 GMT
WORKDIR /tmp
# Thu, 30 Apr 2026 23:52:25 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 30 Apr 2026 23:52:25 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 30 Apr 2026 23:52:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 30 Apr 2026 23:52:26 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 30 Apr 2026 23:52:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:71574deb335f1e823f938f4a215de00a90d63866898f1f354a0b15e8b9c30577`  
		Last Modified: Wed, 22 Apr 2026 00:17:08 GMT  
		Size: 29.8 MB (29840300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72ee46c033b5990060b9acaa5985a11a008290bfbbb27b32d546e2487a9a5e65`  
		Last Modified: Thu, 30 Apr 2026 23:51:37 GMT  
		Size: 88.4 MB (88420341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5e365ad6b822f0672f587fe0ca1d8b89f990afac4d0c85f9c7afebcfe18e3e`  
		Last Modified: Thu, 30 Apr 2026 23:52:51 GMT  
		Size: 73.0 MB (72987256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5fe71a76bb2069146a4a26d7785b09f888bb67b1f3163c902cd9f47dccd389f`  
		Last Modified: Thu, 30 Apr 2026 23:52:50 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e07eb1e7e55a0a5df4833db4f1b84d4cd77acb8cf49fe0c4b7ccb2c4ee1421f`  
		Last Modified: Thu, 30 Apr 2026 23:52:50 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f91838c001d6d0c67b7fb3c32a4a26ef59d50ed08ce459e82ca3759789b39de1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5224880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb51229ab9e746e301ca78998a43d581ec9f683347af2307ecf2611e24361b3c`

```dockerfile
```

-	Layers:
	-	`sha256:1ad391304862cbbe42fe43722da855430b05c965441224191d85dab674badcc9`  
		Last Modified: Thu, 30 Apr 2026 23:52:50 GMT  
		Size: 5.2 MB (5208387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07b5bb66ace9741534efd8617e86b3a17975ba14affcd4f83acedfe0743cb64e`  
		Last Modified: Thu, 30 Apr 2026 23:52:50 GMT  
		Size: 16.5 KB (16493 bytes)  
		MIME: application/vnd.in-toto+json
