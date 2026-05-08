## `clojure:temurin-17-tools-deps-1.12.4.1618-trixie-slim`

```console
$ docker pull clojure@sha256:9f71f5b23d51020613007803b75864e32ca60e53ecc173f5854f12da69c348d6
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
$ docker pull clojure@sha256:f90497c05127b7c6a82caf29b984627b6158cafcca9ac415c4eff3dadf6c7ccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.7 MB (247698055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e9d7cccc36c19c9962843d250e32b9e87ca02a058810b66ec1c706d50ea0d7e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 00:08:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:08:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:08:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:08:04 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:08:04 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:08:21 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:08:21 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:08:21 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:08:21 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:08:21 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8368e7e935ac2925ff5f7180a423198c437049c9b1c36baf375fcef4ec57d226`  
		Last Modified: Fri, 08 May 2026 00:08:44 GMT  
		Size: 145.9 MB (145905439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3dd1c96f95a0e3a3f53675d5ec48f51179e3c2b9439260543d4a1493d3494b`  
		Last Modified: Fri, 08 May 2026 00:08:42 GMT  
		Size: 72.0 MB (72011401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa3ebff89c53fedcb40991ff3823fa399149e8525bd70fca17c5ad99ac62ecf0`  
		Last Modified: Fri, 08 May 2026 00:08:40 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7982ea3707b597121d2c6532dd72f502bfcaa1c804ca9c4059d4ed2c12088c9a`  
		Last Modified: Fri, 08 May 2026 00:08:39 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:aff2189c4cd302a8495831f910b105589cf102e6384657c920d2d395ee832ae8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bb11282e86fb88930c64e6360c71e307c22858e4eecc419941987294bf3d453`

```dockerfile
```

-	Layers:
	-	`sha256:336ad87a8e7ae4921083820d9595dfdf4ca2eef08bd3acf86cc3ec418d591c65`  
		Last Modified: Fri, 08 May 2026 00:08:40 GMT  
		Size: 5.3 MB (5259819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c950b519bf04aba0d2e0b491c9f601ef19d4327dc0a5aa07834723a69b2a0203`  
		Last Modified: Fri, 08 May 2026 00:08:39 GMT  
		Size: 16.0 KB (15966 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b99e113b4a41de25d281cdecdec397b0fac7e08253dc02b8864ef5371c279b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.7 MB (246700486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:123f7f7fc51b24da15bfba3728ff0da4b071dd60241f38e7290f18efc08ac1e6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 00:09:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:09:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:09:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:09:59 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:09:59 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:10:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:10:16 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:10:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:10:16 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:10:16 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3a7cf2b84d811734126f10f3145c40f6dc6c880a8da0d163dc3b57fcaf02418`  
		Last Modified: Fri, 08 May 2026 00:10:42 GMT  
		Size: 144.7 MB (144724334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc6c06d19d48e9376f353d4450b33dc9d942c777ca5189cf773554a705d23ed9`  
		Last Modified: Fri, 08 May 2026 00:10:37 GMT  
		Size: 71.8 MB (71831508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c98e060b460ff91a96fc3a9f16ac5c6d1e9db5c34eabd7c00698f833eff32f`  
		Last Modified: Fri, 08 May 2026 00:10:35 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:420f4480c3459d0ccefc96cdeb08f183e3a4788cf5d41d7353d5004704dcbfb0`  
		Last Modified: Fri, 08 May 2026 00:10:34 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2730c91d808f511b5675b90548a0727631831f896f4808bf2dbc63509a545dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5281672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35400caa4b9940d0c04012a4a91c78bd6ca3ffa6a237ffc628a9582a54fbe190`

```dockerfile
```

-	Layers:
	-	`sha256:eced4348eae287233e6520bd8118e796df282ecc736725568635dfe991b62d6c`  
		Last Modified: Fri, 08 May 2026 00:10:35 GMT  
		Size: 5.3 MB (5265588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:796aa6473fa6eee97d83725bba59e46126c270e0adb8b923a991acb6f8c86295`  
		Last Modified: Fri, 08 May 2026 00:10:34 GMT  
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
$ docker pull clojure@sha256:52b5e17a373a04d89d7beee3805b9c9fb6aead449086bc5a769a7c2e5548df53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.5 MB (238455422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55cb4472130ba3d5f63dcfdc4585e5a8dbc3e073f9577c688f6df2f3b65c3bdd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 04:01:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 04:01:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 04:01:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 04:01:03 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 04:01:03 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 04:02:25 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 04:02:25 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 04:02:25 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 04:02:25 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 04:02:25 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:71574deb335f1e823f938f4a215de00a90d63866898f1f354a0b15e8b9c30577`  
		Last Modified: Wed, 22 Apr 2026 00:17:08 GMT  
		Size: 29.8 MB (29840300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150332b9769a3e50f47d036c734faa3f383f8ddacfb44d5dcc29fa64b02ecdae`  
		Last Modified: Wed, 22 Apr 2026 04:01:47 GMT  
		Size: 135.6 MB (135627000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed07a87de185171280320c8bb7216ba61fd3e71db135ce5537da4a19f2bbea67`  
		Last Modified: Wed, 22 Apr 2026 04:02:51 GMT  
		Size: 73.0 MB (72987082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873213f0ba4721a51f43092b62ecb6315412a423d5ec7151cc2a1d9320057d9f`  
		Last Modified: Wed, 22 Apr 2026 04:02:50 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8967983ac424ebaa33dfb9ae561201e64c011368a583177a19fab59b3e3c5e1a`  
		Last Modified: Wed, 22 Apr 2026 04:02:50 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0db0673300dd5f4eca88f1a355610596a691391d214a357f7f894d2d93a54486
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5270928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15ada69889849da62564b6d52e611d161cb0dbc64b492a4d94a39756291526c1`

```dockerfile
```

-	Layers:
	-	`sha256:4f86e969552116e6bf82f6e1846a21a4c5d611a715bc0851182151c013df02be`  
		Last Modified: Wed, 22 Apr 2026 04:02:50 GMT  
		Size: 5.3 MB (5255116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69e742f00a8496439e92785f33745bf8f4a1e2a072f0f0ca211338c981d07711`  
		Last Modified: Wed, 22 Apr 2026 04:02:50 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json
