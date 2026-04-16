## `clojure:temurin-17-trixie`

```console
$ docker pull clojure@sha256:e3109e2b285867d6af3d2de6be0209c9bd28d759492a75218f830926bd503e2c
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

### `clojure:temurin-17-trixie` - linux; amd64

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

### `clojure:temurin-17-trixie` - unknown; unknown

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

### `clojure:temurin-17-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:50f7f003b8f8f00156f17ba1b3e348ff8f9352e6da0a5e02162570ecbf3b5866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.4 MB (283355735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1fb9979122e6fc5ff2ad8687c7396ade2f5df083886b00272d2f5fce53f05c9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Wed, 15 Apr 2026 22:15:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:15:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:15:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:15:48 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:15:48 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:16:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:16:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:16:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:16:06 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:16:06 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:912041a7b9f63b6550d3a3949c43e45f74a36a2f80c727e70e41cbe851de2d20`  
		Last Modified: Tue, 07 Apr 2026 00:11:19 GMT  
		Size: 49.7 MB (49665256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a79c82f762b84c7085a4f60befd1fa4179b431b75a40772402a0f5164d6c39f`  
		Last Modified: Wed, 15 Apr 2026 22:16:32 GMT  
		Size: 144.4 MB (144436242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97186f4d450f1d702cb0de83176d636d3b9f9c168771b718693db487ea217570`  
		Last Modified: Wed, 15 Apr 2026 22:16:31 GMT  
		Size: 89.3 MB (89253199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d8252a23ad64da26a4c7855504e3af875130bc7ea24b5cb07c8cf836bde1d2`  
		Last Modified: Wed, 15 Apr 2026 22:16:27 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4c8b20efa767047d7bfcd56f727bd0173f3ac33cde8a86f98fed0be32685cd7`  
		Last Modified: Wed, 15 Apr 2026 22:16:27 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:9aa246cc7336dafaa05b1ae1d0dce6f9003cec63890320132ae8f58cd8f0446d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7493569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca937ed38e5118b862ecd736c5014a9cad64a4b9a8be8be0ddeb12b0223929cb`

```dockerfile
```

-	Layers:
	-	`sha256:c3b0858c072a801664a32868c8736a3ebd11bbb13ebd15ff30836dfe0a335c14`  
		Last Modified: Wed, 15 Apr 2026 22:16:27 GMT  
		Size: 7.5 MB (7477697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c44c6e059640e2e6aa775bf15b052937c9baf0d44912f36afe00fda3fa078e69`  
		Last Modified: Wed, 15 Apr 2026 22:16:27 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:fc24b6887061df4bc5bd92bd03ae9f2cf1661eda794196a29990dd07f9139e6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.3 MB (293280260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12e0877a2b0aa4591426ffa6d8349b422f5702851abb77e9fc929f40ff018d0c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Thu, 16 Apr 2026 02:51:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 02:51:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 02:51:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 02:51:45 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 16 Apr 2026 02:51:46 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 02:57:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 16 Apr 2026 02:57:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 16 Apr 2026 02:57:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 02:57:23 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 02:57:23 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f2bea5beaa06af8495b6a91d35dc5ce3b11a84dad25d5c0a468a1e7008ed9e62`  
		Last Modified: Tue, 07 Apr 2026 00:12:52 GMT  
		Size: 53.1 MB (53118669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d63fa71f8a08634b0312e1df11dd8fc3363471d8c3e45af52999c7c3ba56e4`  
		Last Modified: Thu, 16 Apr 2026 02:53:12 GMT  
		Size: 145.4 MB (145438287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f4f8ab741da512d80931a6a079143eadd8b6c2ede80fcd81c7b7fc15028c80`  
		Last Modified: Thu, 16 Apr 2026 02:58:17 GMT  
		Size: 94.7 MB (94722259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd1e215df1b1fc90d8e238c08e8a00506699e11a949d47283f46b167155918d`  
		Last Modified: Thu, 16 Apr 2026 02:58:15 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045a83e090065c566f36f08d430100cb9bc688b6f69fcd776c3dc42d6d26fb10`  
		Last Modified: Thu, 16 Apr 2026 02:58:15 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:59ef7dce9a92ae6986910399b37dca4a6952ef4a8f4c886d03d02b7b8fefbfed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7490887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98facbdbe0b0baecfc782b4c659c74c04e214cafe813c9c3d873063b1c6844d3`

```dockerfile
```

-	Layers:
	-	`sha256:c08fc8bc92a5a7637f03b181c6c29b4a2631c4a6365c0f01c3ab8916eb66f649`  
		Last Modified: Thu, 16 Apr 2026 02:58:15 GMT  
		Size: 7.5 MB (7475088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8a0f943d96b65c3edef091d5f60d82af3c76c357a5b6671f68c5dd752fd8ee3`  
		Last Modified: Thu, 16 Apr 2026 02:58:14 GMT  
		Size: 15.8 KB (15799 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; riscv64

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

### `clojure:temurin-17-trixie` - unknown; unknown

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

### `clojure:temurin-17-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:42baab8fbc4dcd60b3828affb2546af8e0593641560e33cb5920d0f1408aff13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274703642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:805dc7c986fe4e912065d9629245c43da138e4bde776a3d082070c7efc6590be`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Thu, 16 Apr 2026 00:40:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 00:40:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 00:40:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 00:40:06 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 16 Apr 2026 00:40:06 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 00:40:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 16 Apr 2026 00:40:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 16 Apr 2026 00:40:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 00:40:23 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 00:40:23 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:99ccdb9e0b0ce79a36cbcc433fd972b049c1e4e84d217954de0e89224b1fb094`  
		Last Modified: Tue, 07 Apr 2026 00:13:49 GMT  
		Size: 49.4 MB (49365104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a6479948f30389f45be50a1b625521e9d73b9d87a964dc77b74df7d56d2918`  
		Last Modified: Thu, 16 Apr 2026 00:40:56 GMT  
		Size: 135.6 MB (135627004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d55540a3577121e5fee641560de9fd623ac07939e4e7e3570fcffafdff4664a6`  
		Last Modified: Thu, 16 Apr 2026 00:40:54 GMT  
		Size: 89.7 MB (89710491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df372882402ad98acee2ba5a63e5ed855db02caf8f4657f81ddc69f3e149652a`  
		Last Modified: Thu, 16 Apr 2026 00:40:52 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9531fcad809e80f1b7f220b7daa70b184e347e77b4254460c4c6834d8a126608`  
		Last Modified: Thu, 16 Apr 2026 00:40:52 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:0b8bb6c699dc7f3cc4a7e4f28737d64da72761b0f902ddb222a267cb3523c719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7482343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b695d8899ada382f8f85211490e160669c04bc33ec39256046add0a3c706c2`

```dockerfile
```

-	Layers:
	-	`sha256:d01523b48410813f814ae6305f6ddecf735528552e2b088cc3d874cce41fc7aa`  
		Last Modified: Thu, 16 Apr 2026 00:40:52 GMT  
		Size: 7.5 MB (7466589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd63c64633e30285f736b45995fc4eea006337421437474302fe0e26a25b3ccc`  
		Last Modified: Thu, 16 Apr 2026 00:40:52 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json
