## `clojure:temurin-21-tools-deps-trixie`

```console
$ docker pull clojure@sha256:8a79a56914d3bdbe68ee659d021c880ab8a41768140b233203e67a736be59671
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

### `clojure:temurin-21-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:34b9f1e51b2542c6549a5a947f881ca6d96869b6ed45c6a0bf3c54a4f0164c0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.2 MB (296237670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3057e47d15e7b4577dbbc3a795bf3a0fbbe9d78c2010b751b6a5c53e25a7ecde`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Wed, 15 Apr 2026 22:05:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:05:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:05:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:05:44 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:05:44 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:06:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:06:02 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:06:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:06:02 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:06:02 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a7730063fcfe708b222d34c4f07d633dfe087a28c05c4daaab2fa9943854c155`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 49.3 MB (49297833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f427bbbb867b2b2dc3ab0babbdf602f13b9f8b60852d627fff571bb895d2489`  
		Last Modified: Wed, 15 Apr 2026 22:06:32 GMT  
		Size: 157.9 MB (157857082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c573e667d4aaa6a21f40e1f22bb791e3143aa244eba7adf30b2ce7d6343b8be`  
		Last Modified: Wed, 15 Apr 2026 22:06:31 GMT  
		Size: 89.1 MB (89081712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e41040bb11c9d8b60dcb2be12a2f9c09765d84d6ffe26598604f3beb90316a9`  
		Last Modified: Wed, 15 Apr 2026 22:06:27 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a0fc601d6e073ce3014732d4dcf0edd2250a40873036309a3fb31f67cf4c82`  
		Last Modified: Wed, 15 Apr 2026 22:06:27 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:aefb1a9375b65cf4127bbd9be16a4f871bf87ce727982bfab2d80c363ab4fb33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7488273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e96ae7b513a3ecd0230bb0a3e13502bde26187b139696188f40722d30232c78`

```dockerfile
```

-	Layers:
	-	`sha256:a4b96918a320da06a7b52be91298e3548d344dcc2a2fd08398aafb1d16ba053f`  
		Last Modified: Wed, 15 Apr 2026 22:06:27 GMT  
		Size: 7.5 MB (7472519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfa74168a5e5f796fa8089d6525eca59b040cde3787c7e7e9c8ed491a9dfbf2d`  
		Last Modified: Wed, 15 Apr 2026 22:06:27 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9eccb5c01c07b7848c85700dea54bccfc2ac460f88ab56afdf260011f8d25fc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.1 MB (295052553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e75595b02bfe3e7fb4a9ee85508ea077853c72f5dd0058ad5d87e2a6e3812d9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Wed, 15 Apr 2026 22:17:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:17:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:17:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:17:21 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:17:21 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:17:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:17:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:17:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:17:41 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:17:41 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:912041a7b9f63b6550d3a3949c43e45f74a36a2f80c727e70e41cbe851de2d20`  
		Last Modified: Tue, 07 Apr 2026 00:11:19 GMT  
		Size: 49.7 MB (49665256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb949a381e324abe6f3fb94813f752bdca08db1d576f8106fa287959017d436`  
		Last Modified: Wed, 15 Apr 2026 22:18:09 GMT  
		Size: 156.1 MB (156133091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4576f8889077122a4cbb5aedfbe3c0c62e50b9ddaf3546479d346a0463c6045`  
		Last Modified: Wed, 15 Apr 2026 22:18:06 GMT  
		Size: 89.3 MB (89253168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b21a08971cc462a1b49052f9d70ee63cf5413713e17108ed473aba47123ec8a`  
		Last Modified: Wed, 15 Apr 2026 22:18:02 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241ad01546f64a687587320f1a0c2e471b63ef1e7e187736b78ebdeb2a0764a8`  
		Last Modified: Wed, 15 Apr 2026 22:18:02 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:0b15e71abb0d8ac0cd14f810fa7a522541a6969fb57c8946580a84871c265d74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7495421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97d58b495b6e03499575065867a701acc561e19abd30b3d473e8a4b90950ea25`

```dockerfile
```

-	Layers:
	-	`sha256:e3502473973a9c0b79172ef926551e7dcaace424604db0d0f8f0800f623a2297`  
		Last Modified: Wed, 15 Apr 2026 22:18:02 GMT  
		Size: 7.5 MB (7479549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:346e40c50a57576455407ffc9b8d57ff1864858aeebf2b2fbc669443c48da18c`  
		Last Modified: Wed, 15 Apr 2026 22:18:02 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:59e31c73513f119ee431c54503a0d8b11bdfd586f3611d43e6c18f4da6524c66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.8 MB (305819264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c600f3ea9e955c6d3c08e1fe9827200f5ea45912bcef2df9d4ead8926d84eb09`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Thu, 16 Apr 2026 03:01:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 03:01:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 03:01:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 03:01:40 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 16 Apr 2026 03:01:40 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 03:07:31 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 16 Apr 2026 03:07:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 16 Apr 2026 03:07:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 03:07:33 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 03:07:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f2bea5beaa06af8495b6a91d35dc5ce3b11a84dad25d5c0a468a1e7008ed9e62`  
		Last Modified: Tue, 07 Apr 2026 00:12:52 GMT  
		Size: 53.1 MB (53118669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb5605a6e452c48331997194aeebeaa58faccfc0cd45ba29af35316c69a1fefd`  
		Last Modified: Thu, 16 Apr 2026 03:03:21 GMT  
		Size: 158.0 MB (157977558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ccdfbab45476b6830016a629408cef747ae4f3c54bdc2811fba7d1468907619`  
		Last Modified: Thu, 16 Apr 2026 03:08:17 GMT  
		Size: 94.7 MB (94721995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af2d35b02fbb3bcca2b6e61d35db3fcb02cb586d86b57762bf5cfb109e430f4`  
		Last Modified: Thu, 16 Apr 2026 03:08:14 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8af850d5443a0338022924395fdfc39c35122234960853f8002e58948e9ace4`  
		Last Modified: Thu, 16 Apr 2026 03:08:14 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:13870b18edd5c572305ffd3a0605acf189b7ba585c86955b10d98ccd97286817
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7492742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b061065a2b668fe4508a4abc6959d44916168dd059dd34751694c0075d352d0e`

```dockerfile
```

-	Layers:
	-	`sha256:6c42d55328b11a11c7026240f08091a86aa097f190c35ec66849728474ee0806`  
		Last Modified: Thu, 16 Apr 2026 03:08:15 GMT  
		Size: 7.5 MB (7476940 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53940cce0e3a8e66dcc07739e67aa8d3bc160552cf3f31cd8ff4f7e84993f9ed`  
		Last Modified: Thu, 16 Apr 2026 03:08:14 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:d34b22bdc86e33a077ee6a908b50e2a042cbb699cd20e319a86086678d9dc697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.6 MB (292641563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c06b8950d257f1d5b5a17ce8bcf3d2afe1d19ac09b6c58f2a0eec3f551488844`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Sat, 11 Apr 2026 21:53:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 11 Apr 2026 21:53:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 11 Apr 2026 21:53:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 11 Apr 2026 21:53:48 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Sat, 11 Apr 2026 21:53:48 GMT
WORKDIR /tmp
# Sat, 11 Apr 2026 22:17:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 11 Apr 2026 22:17:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 11 Apr 2026 22:17:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 11 Apr 2026 22:17:07 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 11 Apr 2026 22:17:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3e61abfb88ee12dd42b3c32c20825f42c0eae3286fe2a9301e326413688c3d40`  
		Last Modified: Tue, 07 Apr 2026 01:54:08 GMT  
		Size: 47.8 MB (47792626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2e07983918932b6a7d3f5b469a0f96350899d0eb2de01a34ca1ec47825c8ec`  
		Last Modified: Sat, 11 Apr 2026 22:00:22 GMT  
		Size: 157.2 MB (157216895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5c3fbcd1550ee670a60daef1c1cc4e18d05de1f5d53f685e084a7f4235d8930`  
		Last Modified: Sat, 11 Apr 2026 22:21:42 GMT  
		Size: 87.6 MB (87630995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d96a7ec307bf91841b506ad983cb90e7ced82d61cd935c75896dd8ba14a69661`  
		Last Modified: Sat, 11 Apr 2026 22:21:28 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc88da63731dfd3eeb89ed6ae01121df828a9dd548a17954e6c66052bcb2297f`  
		Last Modified: Sat, 11 Apr 2026 22:21:28 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:6e25ea3fc8054b6116f66023fd7a3230959b471639f474e14863cf4a2bb5f1c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7476236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0676933f217b4d4bfd7bac23a4e4736719a7f5cb4b464515c67d2b51c7354650`

```dockerfile
```

-	Layers:
	-	`sha256:a7404d78dc5debcddeb123020796a1ddc9ea40e051df2a598c64751e9ee21d1d`  
		Last Modified: Sat, 11 Apr 2026 22:21:30 GMT  
		Size: 7.5 MB (7460434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b25d07d74d2dbd0b533305a2bc150f7af2570a0faf1f97d357e14a770fade971`  
		Last Modified: Sat, 11 Apr 2026 22:21:28 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:ebc37b4ddf9db9ba0363c64317335b8ff336c5ae6142f7e732452eb90c0c0c8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.2 MB (286181774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb9ae2472d64addf7c807c1eabea1cae47e91643e811c01b85d575ba4da015ed`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Thu, 16 Apr 2026 00:41:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 00:41:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 00:41:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 00:41:46 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 16 Apr 2026 00:41:46 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 00:43:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 16 Apr 2026 00:43:15 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 16 Apr 2026 00:43:15 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 00:43:15 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 00:43:15 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:99ccdb9e0b0ce79a36cbcc433fd972b049c1e4e84d217954de0e89224b1fb094`  
		Last Modified: Tue, 07 Apr 2026 00:13:49 GMT  
		Size: 49.4 MB (49365104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e022bafa62bda64d6a51a016ec92ced7e9445747c5f54cb72881b028f644c812`  
		Last Modified: Thu, 16 Apr 2026 00:42:30 GMT  
		Size: 147.1 MB (147105267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d81c70890d0a7e62ee653e8f8d2b5882dac91b9a443de5cb1bc060e2aa90d68`  
		Last Modified: Thu, 16 Apr 2026 00:43:45 GMT  
		Size: 89.7 MB (89710361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce259bca5cb5427091d901e18a5ceb30b5782daab188414da3943a3ac887332b`  
		Last Modified: Thu, 16 Apr 2026 00:43:42 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0690b95bcf534561b46d33ae6140098999ee774de23f23b19084ac1cb4860c`  
		Last Modified: Thu, 16 Apr 2026 00:43:42 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:8167dd000fd80c459677262c06a5d0712303836aba86bb2c489a68da2378c744
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7484195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb9becb20c839cd9423edff921dcb79ecb04acb1f084d039f773e28df1d11b8d`

```dockerfile
```

-	Layers:
	-	`sha256:28fbcd06a9fb0886ce42b17aa5e65b95ae7b71bc22327632fb5bfbc2245c7c20`  
		Last Modified: Thu, 16 Apr 2026 00:43:42 GMT  
		Size: 7.5 MB (7468441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da4362bcfc5c4fad6acd16365720b81cf1779d426b03ac8a1631d362907c670c`  
		Last Modified: Thu, 16 Apr 2026 00:43:42 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json
