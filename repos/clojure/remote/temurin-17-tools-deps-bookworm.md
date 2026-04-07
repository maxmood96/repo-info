## `clojure:temurin-17-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:b33604bef667d7764c405e5d9a75002ec6af673cc518bbbc2b916fd141bf8394
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

### `clojure:temurin-17-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:be9aacebc2aad945d05fddeabc44e863c073bdb91a15e7101e5deb49479f5bab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275295662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a23ddae75f329da080710d022b420cc2ca29714e5201e2bb54050ff111b0e6c3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 03:14:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:14:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:14:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:14:44 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:14:44 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:15:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 03:15:00 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:15:00 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:15:00 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:15:00 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb09094347c806548d10c9ee4414195afd9c68440d9da76168e6b34bafd715d3`  
		Last Modified: Tue, 07 Apr 2026 03:15:24 GMT  
		Size: 145.6 MB (145628717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb9bb03ba75050eef18eb6406d95b1f2a0c3037078d401d95fa070f240df49b`  
		Last Modified: Tue, 07 Apr 2026 03:15:22 GMT  
		Size: 81.2 MB (81177080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:274f93aed937f2634b96be995aefcb62a98eb033129ffe3addfbcbcb8728ee6c`  
		Last Modified: Tue, 07 Apr 2026 03:15:19 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ab7555909f9366a092bc12f6fd3f13eee7cb83ecb2433dce809c396ecd2d2e`  
		Last Modified: Tue, 07 Apr 2026 03:15:19 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:2da0bae60694a2aa4d829142511fcc72a3b2594f4ebdc6a3c06779a3f6fcd764
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7394080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6329a214f1bb67b774f9eff0ad5066f71c1d188f00033bb6a0a4eed023199adb`

```dockerfile
```

-	Layers:
	-	`sha256:bf1d76f27a749e05799293113e31c00cc0b24d31171a3b878d8200dd02e9d970`  
		Last Modified: Tue, 07 Apr 2026 03:15:19 GMT  
		Size: 7.4 MB (7378302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d664fa9f52dda7b4bc4c5e07e5db5a747d8b6dc6bc272277d80ee90d42de83e`  
		Last Modified: Tue, 07 Apr 2026 03:15:19 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b9229a013d78f3b34b5684c882439ada194d8637d1ccff5f552d8ed0ad72df03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.0 MB (273969003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a56abbcfba60562ba4039857eb03b235a459b2cc474059a1ed6abd4abd9e163e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 03:25:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:25:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:25:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:25:44 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:25:44 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:25:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 03:25:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:25:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:25:59 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:25:59 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a5640f6d669bd0b44f1458a8caac2a42f65ba877ec921985b35ea3014b6f49`  
		Last Modified: Tue, 07 Apr 2026 03:26:21 GMT  
		Size: 144.4 MB (144436224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:772bccb823acc039efb828b9ed24d2474323c72b1d7bfc7b0f4b7e612c67212b`  
		Last Modified: Tue, 07 Apr 2026 03:26:22 GMT  
		Size: 81.2 MB (81158474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714a31aa0f893068c76366e8048e57212ebf4ac4c3199d71956ca1472043a3aa`  
		Last Modified: Tue, 07 Apr 2026 03:26:19 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f655425a74c45ce6e042136be130a23fa4bb0e17fbd248bc0e8986ea35441c1c`  
		Last Modified: Tue, 07 Apr 2026 03:26:19 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:737f54f834f31ccaf63d9137da5dd37ac913412f6e168e53ac03fe3522ef8a9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7399961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d25cf4c302a61714ef220bf1a8cc7f022c136f4ff9bdff69eaf243b80cf2219b`

```dockerfile
```

-	Layers:
	-	`sha256:93ee0cf18dea5efc3e1fa63e8ce3d3dbafbc348d818f0d1234c33bfbd7a05330`  
		Last Modified: Tue, 07 Apr 2026 03:26:19 GMT  
		Size: 7.4 MB (7384065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e355f44d0f3f160d5d76caee76be1c9d1081e342bbcbed5e038674188b222b73`  
		Last Modified: Tue, 07 Apr 2026 03:26:19 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:b58db38cb4275cc283daa6aeb32f21573afe857d136ac02b5571a2096c8faf09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.8 MB (284776015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1049bee248abe681aba87b419861a6da70ba6db2a3c02e9175733c374ddbe5de`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 18:24:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 18:24:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 18:24:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:24:37 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 18:24:37 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 18:30:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 18:30:17 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 18:30:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 18:30:17 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 18:30:17 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c072e92b832614e86d956c6381c6b7617944feae3193ea5691e9506870844136`  
		Last Modified: Mon, 16 Mar 2026 21:51:19 GMT  
		Size: 52.3 MB (52336698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ee64ed0afeae873fd2f06096ddec7906316112c3693f7c534e02be26621b37`  
		Last Modified: Tue, 17 Mar 2026 18:25:57 GMT  
		Size: 145.4 MB (145438236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc3621686d4d4130cc10a6034d7a29a7ac3ebf82d6e3c02fce07e1c8477c04e`  
		Last Modified: Tue, 17 Mar 2026 18:31:01 GMT  
		Size: 87.0 MB (87000042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1db6b7fac07fec680ca092b5be38f1d8b2374f355e66445f9da98cf57505b4c`  
		Last Modified: Tue, 17 Mar 2026 18:30:54 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f562593312ad2a3a137ba4daba01aa5abe410fafcea2686e6069e54c6e5240d`  
		Last Modified: Tue, 17 Mar 2026 18:30:54 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:e02c700d8a570a003384471a532656451c0e456db201cfccd45acf2bf030baa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7399344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:886fbd23342622a9184ad1a15593d65235e682869b1e802e4557effc743e2c2e`

```dockerfile
```

-	Layers:
	-	`sha256:4bfd444d8e0c99348c157544462180cc88e5bc02b38efd25f9e92728ecea2479`  
		Last Modified: Tue, 17 Mar 2026 18:30:59 GMT  
		Size: 7.4 MB (7383518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b8ce5b92ae902badd96b49dbbc724ca5d2821c803005901e6eca4f407a4442a`  
		Last Modified: Tue, 17 Mar 2026 18:30:58 GMT  
		Size: 15.8 KB (15826 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:e2a710701f1b6955f34cb6ff4536fa55c22c922dd6826008133c33d47e469032
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.8 MB (262764440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96191873ea5d50f1e1e07439e913dfda1b87c236fc22da56c816ec8a0b868b89`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 05:42:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 05:42:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 05:42:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 05:42:49 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 05:42:49 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 05:43:03 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 05:43:03 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 05:43:03 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 05:43:03 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 05:43:03 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:40ecbf1d4e17f6b072e6cef463823baec601d9f21c9dc33d98bd258448a986f6`  
		Last Modified: Tue, 07 Apr 2026 00:10:32 GMT  
		Size: 47.1 MB (47148084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30386c1a9a679281d9dbcfe1187ba3ef51a1f5825055d1c84b6336c179be5344`  
		Last Modified: Tue, 07 Apr 2026 05:43:34 GMT  
		Size: 135.6 MB (135626801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7281f00443a9c179f688356ffd078e1d9a310e3e67ff5ff3388ddab19f423266`  
		Last Modified: Tue, 07 Apr 2026 05:43:33 GMT  
		Size: 80.0 MB (79988515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dca601ff6c924639bbf4cff951b047327fef4fcc498cf38cdc6a668cb4145dd`  
		Last Modified: Tue, 07 Apr 2026 05:43:31 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cca82ee843d5953f936b9bc446200b275a6ac33d433fd1313d9dd1aca0a47b`  
		Last Modified: Tue, 07 Apr 2026 05:43:31 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:09f3eaa0ecf3dd257c1d5eb5f158204be8a8ca4a279e3db210d8b22fd5be7421
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7385398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3050d8763d81288715bb7ccbe0f87c8bd1a84bd1700f965dff20281e1e5c732`

```dockerfile
```

-	Layers:
	-	`sha256:2faf2eca202154050a3103a693bf97ae86c7f1a9ac922ed75c21f663e4e272ed`  
		Last Modified: Tue, 07 Apr 2026 05:43:31 GMT  
		Size: 7.4 MB (7369621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac0dd3456d381910f3e6a2cdcdc715dd9f79337fbd1724d20dd1d7b5928b8440`  
		Last Modified: Tue, 07 Apr 2026 05:43:31 GMT  
		Size: 15.8 KB (15777 bytes)  
		MIME: application/vnd.in-toto+json
