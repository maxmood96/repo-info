## `clojure:temurin-17-tools-deps-1.12.4.1618-trixie-slim`

```console
$ docker pull clojure@sha256:7f4193d2e18f03ece8fe2c674a1f3b030bdb1454c9dfd5ae1c048d5a533f0ba6
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

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:55248bd5728243c82aa5eca9db37b2333acf37a4947fd6198061ded73aaaaa5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.7 MB (247698274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36ce050ca1d2519f49099b539c9917822ea6cb2b5b056628af17c2436725cd0c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:17:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:17:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:17:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:17:27 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:17:27 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:17:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:17:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:17:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:17:44 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:17:44 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c930bc4831dd6b6f9559335b39bd617bbd0a80452db29da1d500a22f842ebb80`  
		Last Modified: Fri, 08 May 2026 20:18:06 GMT  
		Size: 145.9 MB (145905489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68eee162dc24ffc04347952d46d204632367a8383891dabf6d69857dbdc487f3`  
		Last Modified: Fri, 08 May 2026 20:18:04 GMT  
		Size: 72.0 MB (72011519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5fcb578a47b2b839c8017ececae0abd20c92d17a2e403d573a839979d508f57`  
		Last Modified: Fri, 08 May 2026 20:18:02 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ca3709de0e0a46c68a8efa9d10425b88eac1c384cdab602c3857a16f1a4407`  
		Last Modified: Fri, 08 May 2026 20:18:02 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1749c6fb2024e5f6c3040dfe48ce33e92c0d7385be47d4481fd1177e862178b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed3098aa175c3f25ffc42f876306fd85096de4a7eaff18fc1b12fae860543abd`

```dockerfile
```

-	Layers:
	-	`sha256:d80e9caa5f8e501606e7a117acd947998aaa2e266ccf7e4a1d25b59c01086708`  
		Last Modified: Fri, 08 May 2026 20:18:02 GMT  
		Size: 5.3 MB (5259819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e65af8a3ececd0f3a38c7b9c3634c369ef3aa912e73fd2536acfc328495907bb`  
		Last Modified: Fri, 08 May 2026 20:18:01 GMT  
		Size: 16.0 KB (15965 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3c13779965a0119db7ad6b46a6ed750aeac7c4e35dd21deefe074f950af1bd46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.7 MB (246700700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f8e033e635918b09d0cf76cd4d8730b061dfbf02470fdef9b0d5685e74ec9e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:22:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:22:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:22:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:22:02 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:22:02 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:22:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:22:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:22:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:22:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:22:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac89e0df31ca5932d5b5e96b10616f269b2cd873b0ea60b99d0ced6163273d91`  
		Last Modified: Fri, 08 May 2026 20:22:43 GMT  
		Size: 144.7 MB (144724334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb9f9db97196412140ad62ed2b70f1dac149212f2476d45fe04ea99ddcf5098`  
		Last Modified: Fri, 08 May 2026 20:22:42 GMT  
		Size: 71.8 MB (71831682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91229c9d006bb9a0835db42a71457c0b73f6450a74b3ce8f79ec4cf3cebf4b6`  
		Last Modified: Fri, 08 May 2026 20:22:39 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9675ca45e3f6e207f9281c89cd42d67dacb132ec6b1b3bf611772d6d7b52ce1`  
		Last Modified: Fri, 08 May 2026 20:22:39 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:87a9ed6e2f13de6a421340bf242d50365f76eb46c5600b8b471bc25ccb13c40e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5281672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f5a77d201fb5907efe90fd55592b8d52c07b88f15ab277b70740c425904f93d`

```dockerfile
```

-	Layers:
	-	`sha256:9d8d1cffdabfd1c50a4629d7ba3f0815b6860b799cb2a1bb1c6e4ee33844ee4c`  
		Last Modified: Fri, 08 May 2026 20:22:39 GMT  
		Size: 5.3 MB (5265588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d8ddecfa3b00d7532cbbbd222ac49f16b035d568d44d220943f9c869cc26acf`  
		Last Modified: Fri, 08 May 2026 20:22:39 GMT  
		Size: 16.1 KB (16084 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:21d57f0824d64be890edfdb5789e7cb618e754989d1b9eff31cc74ccaee30f72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.8 MB (256793870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5bbbb0cfb71d82d34e5aeae2a56cbdb2db16bd0bb8883f7cbaddbace5f3448b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 00:45:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:45:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:45:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:45:58 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:45:58 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:53:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:53:16 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:53:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:53:16 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:53:16 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b5fd051d0fcd0789e7358cba300f83befdba943416041497be86050e282a6d02`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 33.6 MB (33598032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:937b7eb5aea1a56bc2fcf2ec92c34b7b899cf187331f6afa218be284e921541e`  
		Last Modified: Fri, 08 May 2026 00:47:15 GMT  
		Size: 145.8 MB (145766229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f25e139c0e3d442e0a526ab9593bcf2a65eaaddac6a02682ada3feea90dd94`  
		Last Modified: Fri, 08 May 2026 00:53:54 GMT  
		Size: 77.4 MB (77428569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f7e6365702509ead0cc28131f0cafc6b909c175ea52e9ada76a8f1237f1a7e`  
		Last Modified: Fri, 08 May 2026 00:53:51 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df182d32e5646108ff40e0cd71cdd6d04ac8797b182504c8f4c63e6e47d8039`  
		Last Modified: Fri, 08 May 2026 00:53:51 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bc8a95d4da36e05eee257a9adade14c02441c567889a03e94cf8d24f344e9b6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5280204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b6a826c13676eb721ba1e3a1139b1dffb83dc53d3aaf555a8c04954e503eeb6`

```dockerfile
```

-	Layers:
	-	`sha256:541dea9f58f18e6c41ae812e16d26f136ea9356347229a32ae96a217702e8a37`  
		Last Modified: Fri, 08 May 2026 00:53:51 GMT  
		Size: 5.3 MB (5264190 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2601d96cb98f75c2a99325c413fb64c268681d4e691966b6222e4c459035586`  
		Last Modified: Fri, 08 May 2026 00:53:51 GMT  
		Size: 16.0 KB (16014 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:fda268f2fcf1f52d6b4da382777d6bde19b7a53eab96e64eddad3a72ce2c7f2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.8 MB (241844799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dca98f4052e745619c647932ade947765d291464cef7425175f75b0a30ed7782`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Fri, 24 Apr 2026 17:48:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 24 Apr 2026 17:48:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 24 Apr 2026 17:48:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Apr 2026 17:48:07 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 24 Apr 2026 17:48:08 GMT
WORKDIR /tmp
# Fri, 24 Apr 2026 18:05:14 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 24 Apr 2026 18:05:15 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 24 Apr 2026 18:05:15 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 24 Apr 2026 18:05:15 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 24 Apr 2026 18:05:15 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:839a829e8fec6662efa3cab7ad2470690879a00890c2cd0f31b7ec868d89805f`  
		Last Modified: Fri, 24 Apr 2026 17:53:53 GMT  
		Size: 142.7 MB (142662943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914e5777c69f98dbff6809d04c36a53b6f6ce0985215d06f9ff3afa6034b9063`  
		Last Modified: Fri, 24 Apr 2026 18:08:54 GMT  
		Size: 70.9 MB (70900618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6102cb1b86fa4e2d79aa3d441bbb465ec05520a3c193df1725a9205d66ca0a`  
		Last Modified: Fri, 24 Apr 2026 18:08:44 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b4a64cf61225ece717217cc9ac4ee192e5daf83b11cd4c2515f3088534274a0`  
		Last Modified: Fri, 24 Apr 2026 18:08:43 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3f3a37f8172863b6916c44cefb6f5da891135bb527da542feaf808c78d4538c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5262597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c72d9b61a8e858e0439c3f1d70221f7852c5d1d0539912ea8b827ee52b192951`

```dockerfile
```

-	Layers:
	-	`sha256:1717073c0fd98c52768d838d5ad5298a84c54c15ff5942df263b1887fb7ea2d3`  
		Last Modified: Fri, 24 Apr 2026 18:08:44 GMT  
		Size: 5.2 MB (5246737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dde60a45455ecb9c13cecc3a49e924765b2c19b0c1118da5205b80f1f52d28a9`  
		Last Modified: Fri, 24 Apr 2026 18:08:43 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:d988ff4d4e73336a6602a9c7a3d6bc27e892a553167a0e078ee3a09076d4b8b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.7 MB (238738927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca542384c0d1a2a3414f201a70c637772110b1f19b9126a628123ef4e6671cf6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 22:15:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 22:15:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 22:15:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 22:15:44 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 22:15:44 GMT
WORKDIR /tmp
# Fri, 08 May 2026 22:16:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 22:16:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 22:16:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 22:16:57 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 22:16:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2fbbc68c452b3ba3a496488f38159dac53afe693311bee1c04f555d854ff4a2e`  
		Last Modified: Fri, 08 May 2026 18:29:20 GMT  
		Size: 29.8 MB (29840347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512e6532304b09c89615bfcfc7e7795be56d90f51435c3bb6a021ae95aeb07f6`  
		Last Modified: Fri, 08 May 2026 22:16:23 GMT  
		Size: 135.9 MB (135910435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c01768e72fdf9f1c974d380959173675a06997b6d457ff415e56bd565caa57`  
		Last Modified: Fri, 08 May 2026 22:17:21 GMT  
		Size: 73.0 MB (72987105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8c1bcf05e1b511f5a47979af9130ba7591dfe48d6f049e7ec3361c9284b464`  
		Last Modified: Fri, 08 May 2026 22:17:19 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d55ae1325ac3ad70ea6c3539b2c68b3d25feb325ff24b9bf6db6e5ec2ddc631`  
		Last Modified: Fri, 08 May 2026 22:17:19 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ea19029df9ee045e442b07d93985f0159deaa336862c75955e225e2331c78504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5271709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbb0f51699909fc1bb64e1c2d038b2b7dff948019fd611ce465b429c948f4789`

```dockerfile
```

-	Layers:
	-	`sha256:46ae26c3a95d4e32c159a909e52b94e084bfbb33244f9a8a387493b966ef58b2`  
		Last Modified: Fri, 08 May 2026 22:17:19 GMT  
		Size: 5.3 MB (5255743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea9699fc6573109a5c3a659fb52909d6750abd1fe29a100e5053b6bd7c3053a0`  
		Last Modified: Fri, 08 May 2026 22:17:19 GMT  
		Size: 16.0 KB (15966 bytes)  
		MIME: application/vnd.in-toto+json
