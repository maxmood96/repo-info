## `clojure:tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:9d699f9afd2f0f88f87f8b158389bca5f786d2e7c81c926dbcd5bf7825fbd891
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

### `clojure:tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3ed865c79975060b1ca3f3646ce9b574d8da82d06869c1d793d38f8d00d48007
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.2 MB (190192612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88fab9dbeee57ffceca9402db8ccc049ae1ecee0ad7d35b8f3e1dc29c48e97ef`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:20:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:20:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:20:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:20:56 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:20:56 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:21:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:21:10 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:21:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:21:10 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:21:10 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b940c5a0722435f1b01248646b8ef00a746b25a5dabb6c7326aab8c0c409a79b`  
		Last Modified: Wed, 22 Apr 2026 02:21:31 GMT  
		Size: 92.3 MB (92256332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7572c8e05b05843f7b492531284b5693210b0c5acae8e753716f85c40b4f46`  
		Last Modified: Wed, 22 Apr 2026 02:21:31 GMT  
		Size: 69.7 MB (69698987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcffdefdeb69a2aeba1929c6585cba5694ecddc0375c744c1215d0196e4334fc`  
		Last Modified: Wed, 22 Apr 2026 02:21:28 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e954d2818afe96b816bf4c981188afd56e79b5a79eaf98ed9e9aec81d72088`  
		Last Modified: Wed, 22 Apr 2026 02:21:28 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bb6625620682e5feafe0420c41d73dc1cc72b1a4ae4680a5ba4071b67903f26d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5100784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d69f3246cbfc399d7c6b6e357d418163e5d920ce730885462ccf9ff54c77a13d`

```dockerfile
```

-	Layers:
	-	`sha256:d49fbc22863db468866d3c2bb88356a685909bafdbd3973a93f60f154577709c`  
		Last Modified: Wed, 22 Apr 2026 02:21:29 GMT  
		Size: 5.1 MB (5084261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73e4034c891926b0cbc1942d542e6c3c273924cd4b84a2d464bae402615edcc9`  
		Last Modified: Wed, 22 Apr 2026 02:21:28 GMT  
		Size: 16.5 KB (16523 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:cde2b85ea2fd8c17aa684750285d6d6acbcb721495c60d2355d959b6708c4bbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.1 MB (189097545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37a0a12a8dba712d7c84a1f7e59089c7937f6b85b8033e88854b074919e1bee8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:23:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:23:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:23:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:23:55 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:23:56 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:24:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:24:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:24:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:24:11 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:24:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:46ac7a0b9811e518f6b5a0d52940c913a1a560a8f78b82267804914e50244d2d`  
		Last Modified: Wed, 22 Apr 2026 00:16:03 GMT  
		Size: 28.1 MB (28116114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e61d6cc84296320f757691e0c3d09752c315a06e57c9446f92649ac482b421`  
		Last Modified: Wed, 22 Apr 2026 02:24:34 GMT  
		Size: 91.3 MB (91288276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fa3b0f1f2b27756ef9e35ebac28c37dab9ae4576a3b08d1014a0086cc2c992`  
		Last Modified: Wed, 22 Apr 2026 02:24:32 GMT  
		Size: 69.7 MB (69692117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c61dc2c40d0f7a74574092e23b1565cb833c1f4780b968980070a52472060c`  
		Last Modified: Wed, 22 Apr 2026 02:24:29 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c27b3f90bcffd05bcbac685dcc09c1dc0e41486c770fbdf999303b2f3167b36`  
		Last Modified: Wed, 22 Apr 2026 02:24:28 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8701ea28e23b9cd6894599df62122ca2114fa197def56dbe85bc87c440d8a5a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5106710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:742719c7b3ee570254ec3caa382ae4d0e33a3eba08af8c93d5885b1c3fc21ce4`

```dockerfile
```

-	Layers:
	-	`sha256:fa088b3890533ab88858aee52c0c568aa8602f7983d1f5f0b10b846d86fffcbd`  
		Last Modified: Wed, 22 Apr 2026 02:24:29 GMT  
		Size: 5.1 MB (5090043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57a0dd61b8240dc946ec707448e2d2208503cd889f20bc3a411ea09e8f452205`  
		Last Modified: Wed, 22 Apr 2026 02:24:29 GMT  
		Size: 16.7 KB (16667 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:651c95a7f5b208f47173f6b9c9fde0358af70649233f44b226d0faa4258661ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.2 MB (199242786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8c75b337764760e46cade9d4a4a6f05a42c3b155c0418b0efe515b7b8f021aa`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 19:13:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 19:13:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 19:13:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 19:13:50 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 19:13:50 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 03:12:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 16 Apr 2026 03:12:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 16 Apr 2026 03:12:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 03:12:46 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 03:12:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b1c56220ca211bc9d02f1ed5c589465809676b6ab2cef705f1e2fb8e9726de76`  
		Last Modified: Tue, 07 Apr 2026 00:09:42 GMT  
		Size: 32.1 MB (32078464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:186825ad1954e238f9d41fa43dbe8881cdc35374805d5861befa0e42e394c10e`  
		Last Modified: Tue, 07 Apr 2026 19:15:05 GMT  
		Size: 91.6 MB (91632990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98e50018da8243a9b074e4f217112f41998683abe2200edb270fac370b50bdf`  
		Last Modified: Thu, 16 Apr 2026 03:13:18 GMT  
		Size: 75.5 MB (75530289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0301d95516079bc104e7fa7493070504907385432783624f3487eb2eb15354ab`  
		Last Modified: Thu, 16 Apr 2026 03:13:15 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5408b5dc137a9925c208a1339ac2e9b7326c02d29bcdf6f2cd08c58567e2d20e`  
		Last Modified: Thu, 16 Apr 2026 03:13:15 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8c955f108acf6fa285d665ce3285af69ffc5a76ef4ee7b3b6184b78e31c1e475
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5089328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3360bb0a285227d23c7100c9f51b5935413429f4145555bedd64aedb9d57fc9d`

```dockerfile
```

-	Layers:
	-	`sha256:511798b8f2ba6b8c4bcc2b16da39e1552559bb57c790b5cabb82566d09a34957`  
		Last Modified: Thu, 16 Apr 2026 03:13:16 GMT  
		Size: 5.1 MB (5072743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fffec5a02a1c01f9dc3f6d6504dcc2565d1f8593ecf37567e02f7457389a8b0`  
		Last Modified: Thu, 16 Apr 2026 03:13:15 GMT  
		Size: 16.6 KB (16585 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:6238e44cd4edac9cabb50d0291d84b84d726f76678bd9ceb9ca4cd3bb3b33b4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.6 MB (183639319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec9ca72211b4d9cf28bc44ecf5a4264b9c32c5ea5f4b75bd9c7aed06e79d85fb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Thu, 16 Apr 2026 00:43:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 00:43:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 00:43:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 00:43:49 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 16 Apr 2026 00:43:49 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 00:45:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 16 Apr 2026 00:45:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 16 Apr 2026 00:45:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 00:45:01 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 00:45:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c23087fbbda0d8352ee6b2d159c503459acb89da0eba1729b411ca394e68e292`  
		Last Modified: Tue, 07 Apr 2026 00:10:59 GMT  
		Size: 26.9 MB (26891634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a78ac609f8f046c6a31d61cf5e496d160fb1bf38a5cda92b8f538e5fc85bfd`  
		Last Modified: Thu, 16 Apr 2026 00:44:26 GMT  
		Size: 88.2 MB (88233823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0ec5c98363b0741c220393269c785f74da4bc8f4c8318d3a2879a2b0ca435b`  
		Last Modified: Thu, 16 Apr 2026 00:45:25 GMT  
		Size: 68.5 MB (68512818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:731a36ab7ac149be7871eb0b24f994b47dcc46a3e27698767808ceea9b4d9db3`  
		Last Modified: Thu, 16 Apr 2026 00:45:24 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65df5bda0c960ad8db49f2f61b65342578cf767a8142bd56c147a12b2a86a48e`  
		Last Modified: Thu, 16 Apr 2026 00:45:24 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2e2b4678e591636fafc6af5b0ca5f4cca5e2bf70925d96d65a00469a872ef924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5076667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c5dc25b633e6ad8104000600bc73be253250d270874138b5dfad00edd315534`

```dockerfile
```

-	Layers:
	-	`sha256:22da8d77210cf1f05a06521c4cdcaa48709c0129351a1568650114f0455eef20`  
		Last Modified: Thu, 16 Apr 2026 00:45:24 GMT  
		Size: 5.1 MB (5060144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38aadbb431004a05331fd83df6919530f0cc2969f01c8d09e7680b4a76f068eb`  
		Last Modified: Thu, 16 Apr 2026 00:45:24 GMT  
		Size: 16.5 KB (16523 bytes)  
		MIME: application/vnd.in-toto+json
