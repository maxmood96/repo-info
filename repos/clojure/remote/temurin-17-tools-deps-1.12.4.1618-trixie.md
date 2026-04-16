## `clojure:temurin-17-tools-deps-1.12.4.1618-trixie`

```console
$ docker pull clojure@sha256:153284fde005616815e010f1e8ad2cbe685b0f88a98e28e802f5e12f0b84e671
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

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:9c90d81bcc6b58f36e8cc893c7f9677b669274a4dd805b27eb86d45dd831f363
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.0 MB (284009379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd90eb598105b9e7c18eb8929e70274fd6a174fec1ab6704796f3956c48cb9c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Wed, 15 Apr 2026 22:04:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:04:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:04:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:04:24 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:04:24 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:04:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:04:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:04:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:04:42 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:04:42 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a7730063fcfe708b222d34c4f07d633dfe087a28c05c4daaab2fa9943854c155`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 49.3 MB (49297833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b8ef79b2db274d32acefb5eec08dc02e862b48a65b007b80d97059ccfb7400`  
		Last Modified: Wed, 15 Apr 2026 22:05:05 GMT  
		Size: 145.6 MB (145628761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156a4a944f89992b8a22af0e6b5735176475ac8cf6af2d88688116c19e3c1cf6`  
		Last Modified: Wed, 15 Apr 2026 22:05:05 GMT  
		Size: 89.1 MB (89081742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66ac4fe86f7bb32e87a9ccb7cc21d576fd70eb420dfcd9e4ea43e3f5eea67b9f`  
		Last Modified: Wed, 15 Apr 2026 22:05:02 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b2ca02639d1412c865452707474edca7cd091b283475ce0353953c34800138d`  
		Last Modified: Wed, 15 Apr 2026 22:05:02 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:fba4bacde863503f2cb1d08f1fe9b54ed68f6ddce7354c6cf45652a6525e6251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7486421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37faf5dc3b46b7d375eb001ce14f9f042aa1725a0499fb78d98a0884deea5b71`

```dockerfile
```

-	Layers:
	-	`sha256:81d261e764cbea3b39243b2160ce46f80b88216d6983abd902be95c8db705c1d`  
		Last Modified: Wed, 15 Apr 2026 22:05:02 GMT  
		Size: 7.5 MB (7470667 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c72cc485fd9fd9a0b1f2373fc52c6f4354b877c423fd593cfeee752a641d7150`  
		Last Modified: Wed, 15 Apr 2026 22:05:01 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4438a51405bc0694cd9c87f697491c69d912649a181e6ea8ccb3bca5b13ecd2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.5 MB (279485688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af297c748470ea797a51a402819879bfe9e32eba4d76fdb1d0c6499cbae390bc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 03:25:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:25:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:25:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:25:54 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:25:54 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:26:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 03:26:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:26:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:26:12 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:26:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:912041a7b9f63b6550d3a3949c43e45f74a36a2f80c727e70e41cbe851de2d20`  
		Last Modified: Tue, 07 Apr 2026 00:11:19 GMT  
		Size: 49.7 MB (49665256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99780b28a51709ddd21e604dcfc6034f1e9fb5694e088f78ff893724e562bf0b`  
		Last Modified: Tue, 07 Apr 2026 03:26:42 GMT  
		Size: 144.4 MB (144436226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:214c63e47f8e1ce9bc7ec9fab88686bf21b16247895286ed510b1cbf2dd1cc8f`  
		Last Modified: Tue, 07 Apr 2026 03:26:40 GMT  
		Size: 85.4 MB (85383166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afba83f5648d7f8c2715fd60a6855c75477b2206891f7e155d6d00850d566ecb`  
		Last Modified: Tue, 07 Apr 2026 03:26:35 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06e0bb3f4998ec593e1d60a8ab85e1df4b4aeb27029a000a79076ee85eaaacf`  
		Last Modified: Tue, 07 Apr 2026 03:26:35 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:6b1cad40fed13fd18605408464670582cf46e7fba9d199d1222406f6cfedda2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7493569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7205294098bc9311f588139e4a81484324911676d7d44f215e325cd2d0e79e82`

```dockerfile
```

-	Layers:
	-	`sha256:20b7505163d75e31e73ba4722898fe414d7cf0ffda7d0a3648d774e208aa1bde`  
		Last Modified: Tue, 07 Apr 2026 03:26:36 GMT  
		Size: 7.5 MB (7477697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:792a8db0d4156521ff88bf134e9b1afb3fdc302cfee4a395276ad871e4117ae2`  
		Last Modified: Tue, 07 Apr 2026 03:26:35 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:ed4a3a6da4294418d36cc10973eacd172784ff47c1a85de5308bfb26736ce48e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.5 MB (289545217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a116dbbf2763b11f769a3f7bb778524221c1c5ee5bd626dabff1203290fc934a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 14:39:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 14:39:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 14:39:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 14:39:23 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 14:39:23 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 14:44:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 14:44:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 14:44:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 14:44:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 14:44:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f2bea5beaa06af8495b6a91d35dc5ce3b11a84dad25d5c0a468a1e7008ed9e62`  
		Last Modified: Tue, 07 Apr 2026 00:12:52 GMT  
		Size: 53.1 MB (53118669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a76b0a411921a776a6aa7e333480c75bdb58776d62cc75ddfeb7b455ebd920`  
		Last Modified: Tue, 07 Apr 2026 14:40:55 GMT  
		Size: 145.4 MB (145438242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75447135804fb71e3d513ed66a3c7c9b086abc5ebcdfac0cf77581693feb81ff`  
		Last Modified: Tue, 07 Apr 2026 14:44:53 GMT  
		Size: 91.0 MB (90987264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393c169e5e4f0b37362cf91bdd20a15fd3f74d7c20cadc18319073de1a380e4f`  
		Last Modified: Tue, 07 Apr 2026 14:44:51 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f37ce994f8d76f3f373e1af75f252dcbba6ea810629a9aed01743bb56a24b5`  
		Last Modified: Tue, 07 Apr 2026 14:44:51 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:3bea987772449128db09ec88636db916b62d34bca970cfd0ec8727405852b2b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7490890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0e2643688b4108ea7cb245e1f2343e665bf1a55e6395a5cec438ad38181bb62`

```dockerfile
```

-	Layers:
	-	`sha256:65ba6e8cebad57da8ed14b8c1b2a560a70d537d2d582a3a801d4577947d8243c`  
		Last Modified: Tue, 07 Apr 2026 14:44:51 GMT  
		Size: 7.5 MB (7475088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df7576debbc758fc2bd23ccfe4baf2ee7f196527b946ea88247aef57d0606861`  
		Last Modified: Tue, 07 Apr 2026 14:44:51 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:2ec1d1238740538b11593ea837207633c7e5926c7ece27a46f07513c4fb7d3af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.1 MB (278087827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b50d6006ed4d238747e2bf535787dba70e07637750cf0d95861347cdee99d49`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Sat, 11 Apr 2026 21:15:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 11 Apr 2026 21:15:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 11 Apr 2026 21:15:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 11 Apr 2026 21:15:29 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Sat, 11 Apr 2026 21:15:29 GMT
WORKDIR /tmp
# Sat, 11 Apr 2026 21:37:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 11 Apr 2026 21:37:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 11 Apr 2026 21:37:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 11 Apr 2026 21:37:23 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 11 Apr 2026 21:37:23 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3e61abfb88ee12dd42b3c32c20825f42c0eae3286fe2a9301e326413688c3d40`  
		Last Modified: Tue, 07 Apr 2026 01:54:08 GMT  
		Size: 47.8 MB (47792626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de3586f52f160113005887920f505e18e0518029e2ec38342484f9914d399e5`  
		Last Modified: Sat, 11 Apr 2026 21:21:35 GMT  
		Size: 142.7 MB (142663032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deef7dc1aeb4c8a5bb95bca676e63aaff8b53bb83372052fac227134ccd7965b`  
		Last Modified: Sat, 11 Apr 2026 21:41:55 GMT  
		Size: 87.6 MB (87631125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:302a4d00baffef42c71ff5dd686f96adb17710f7f655036250d251ce87b49885`  
		Last Modified: Sat, 11 Apr 2026 21:41:41 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:871a92b85a4ca82aa5adec1d804b403f6056f867ade3afca787602b68be431d4`  
		Last Modified: Sat, 11 Apr 2026 21:41:41 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b65a8cfbac1447495e9aafadd5cf70caee53b7c1e3c769f729a785433b3d12df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7472465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff79a3d41f3510f642129933aff6774a1619c9348d72d48d553d40edc3f7817`

```dockerfile
```

-	Layers:
	-	`sha256:5805cf948cb76a0cd19f194d2a3fa7454baed55fc760f0d286ef6c4ee9b7495d`  
		Last Modified: Sat, 11 Apr 2026 21:41:43 GMT  
		Size: 7.5 MB (7456663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7c8c8eb517d0d999b7a83062faf0daac8174c3b561a6be3f727f12e06bfeb4a`  
		Last Modified: Sat, 11 Apr 2026 21:41:41 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:f163303f7d2f71753b0aea2a1392138a1cc888e3653c0be4ea97d740cde0efd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.5 MB (271537285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:635e2c39cffd55a05f4471a066e82482357b824e2bc00057720f72f05b2b0638`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 05:42:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 05:42:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 05:42:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 05:42:18 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 05:42:18 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 05:43:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 05:43:37 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 05:43:37 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 05:43:37 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 05:43:37 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:99ccdb9e0b0ce79a36cbcc433fd972b049c1e4e84d217954de0e89224b1fb094`  
		Last Modified: Tue, 07 Apr 2026 00:13:49 GMT  
		Size: 49.4 MB (49365104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5be30173782ac514fe3cc2acff6571642739faff5843cc6d1d0067cb9203c3`  
		Last Modified: Tue, 07 Apr 2026 05:42:59 GMT  
		Size: 135.6 MB (135626852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fca09ee2833a47ae6fea387cb5d65815016ac3269d5f2fa97f9dc7d2d0bd43f`  
		Last Modified: Tue, 07 Apr 2026 05:44:09 GMT  
		Size: 86.5 MB (86544285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ed6606350984a889612232a18bfc823aa6134efb85a1ceb80df3f7bcbd1534`  
		Last Modified: Tue, 07 Apr 2026 05:44:03 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd9bf6b70b67aa4787f7dc8b2b3d7c36ff446c056a9ac76b6909477a7e7f661`  
		Last Modified: Tue, 07 Apr 2026 05:44:03 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:7a4cfa83db351ef6d8a566ef9c4867761430b819c5325b30130f073a0738deda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7482343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6ecad5cf61e4689e00fed9be3ad798c964c658cc1ac101e75dbb8ebe30592b6`

```dockerfile
```

-	Layers:
	-	`sha256:63afe970de3a078b35ecbb5fde1048f3fdcd850e9b443ffc412424a086e04c1a`  
		Last Modified: Tue, 07 Apr 2026 05:44:03 GMT  
		Size: 7.5 MB (7466589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0577f44187c96b37b10dddb17cec65a05d6d233be9df703d38735b43dc357dca`  
		Last Modified: Tue, 07 Apr 2026 05:44:03 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json
