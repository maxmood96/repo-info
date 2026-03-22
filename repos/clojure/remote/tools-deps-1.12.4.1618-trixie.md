## `clojure:tools-deps-1.12.4.1618-trixie`

```console
$ docker pull clojure@sha256:641e002a368e5bb97216f98b5a2f1cccdcb06b22c6b1847054f91d4e1d0adcb8
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

### `clojure:tools-deps-1.12.4.1618-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:6b3f14d1b8bc372242c81cfc0873f1b53e45b37df405280a7ec716cadb968376
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.1 MB (227122305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e3f0ab2107cbc73290be182c3073b572c6b0af5e24aa9a70abf94d7932d59ba`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 03:01:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 03:01:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 03:01:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:01:26 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 03:01:26 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:01:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 03:01:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 03:01:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 03:01:42 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 03:01:42 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8f6ad858d0a46fa8ee628532c70b8dc82d06179d543b0b09ec19fc03d4c5b373`  
		Last Modified: Mon, 16 Mar 2026 21:53:17 GMT  
		Size: 49.3 MB (49297530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc706a59f93d2339934226c726d058fae351c8ef063156495b1bc4ea7ee1c428`  
		Last Modified: Tue, 17 Mar 2026 03:02:02 GMT  
		Size: 92.3 MB (92256299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb00a3c0330057be7664606e87b3e1eeff09806a6df9ba482be1f31e4c49a449`  
		Last Modified: Tue, 17 Mar 2026 03:02:02 GMT  
		Size: 85.6 MB (85567437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd08b160009362b410d236f44611e0f5674645e8b34f4092c189dea97064340`  
		Last Modified: Tue, 17 Mar 2026 03:01:59 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54bd6aa6fba0dcf46d85064bf68f9675bc5688c7a536bb082e6328079ae863ab`  
		Last Modified: Tue, 17 Mar 2026 03:01:59 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b5932fe193896b142ab63247bbcc08bf384bbce4a1416892e606a0dd8d2b445b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7455148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a63a56379b857f3e3025ae8a42a9e49ee02aaf88c9c7c15d64724adc05b7bc6`

```dockerfile
```

-	Layers:
	-	`sha256:9f5e59ef8f9917ff9b0125e57b33563c19e2215ea6195aa8cf37aa26aeb3c9db`  
		Last Modified: Tue, 17 Mar 2026 03:01:59 GMT  
		Size: 7.4 MB (7438733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6ce0196d692a027024712a9fa7a9ddcb2b7cdccbb60fa4b42ba891ecf5af8b5`  
		Last Modified: Tue, 17 Mar 2026 03:01:58 GMT  
		Size: 16.4 KB (16415 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1618-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7d1f7c4933764f7b1d8be5faf443f50447f5ca2f0047a2088f4c5bf3332bcba1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226337599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c974fc2d41a66c8a9d299f13781f583341a43074e5bfcdde5579b4f58212fe50`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 03:06:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 03:06:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 03:06:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:06:01 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 03:06:01 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:06:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 03:06:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 03:06:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 03:06:20 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 03:06:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:deab8db42772fcfeb45003461fe0eb7bf63bdb29199a4fb76242b9493437c28b`  
		Last Modified: Mon, 16 Mar 2026 21:53:03 GMT  
		Size: 49.7 MB (49664953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a552f38485bf4861fd5edfd67eaf117753b7c70ac459b9cd97c6f9da6fde39e`  
		Last Modified: Tue, 17 Mar 2026 03:06:44 GMT  
		Size: 91.3 MB (91288288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8716fd966c830d7b948bf9d25d6e8557d2ea47663e28d9d1078c28ef97eedcad`  
		Last Modified: Tue, 17 Mar 2026 03:06:44 GMT  
		Size: 85.4 MB (85383319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a1ce4bb5935ae3e83c03a3640a7fbdf4aa3d2fcd93a15ec3ea136c67d0a2a3`  
		Last Modified: Tue, 17 Mar 2026 03:06:40 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f151745e52766b0f6de1db357b792c4285fe1887adebfc97d94b2240914f16c7`  
		Last Modified: Tue, 17 Mar 2026 03:06:41 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:983f306249a10531eea7da4214e1c6e65cb3ed0260ab8c8a6c9f9088273253a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7462341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6ce8181c27bead5d4faacf7c3e60029c65615f58427e579300bfc0daf123762`

```dockerfile
```

-	Layers:
	-	`sha256:825c96f58f9ed968562ec24d080b33b8287a81baebf95500cc9592aa9d14ba88`  
		Last Modified: Tue, 17 Mar 2026 03:06:41 GMT  
		Size: 7.4 MB (7445784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:889304047b4805c683aa3d1ac8fd486bcd8edc10cdb8156f372a2f74ce4aa53e`  
		Last Modified: Tue, 17 Mar 2026 03:06:40 GMT  
		Size: 16.6 KB (16557 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1618-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:0b5ab1cc319e6b2439345bf63724e4b26485a6f68923c0612568b7f76b3406dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.7 MB (235739541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f2175f3a5e616090bf2c3c39bd33341a314316c3d55dbf15c01c18e3f8ee001`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 18:45:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 18:45:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 18:45:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:45:53 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 18:45:54 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 18:49:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 18:49:51 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 18:49:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 18:49:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 18:49:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:616ed6c40b4f1136ebcda954e46e021bcee567aad248468321da4f4065f4a14d`  
		Last Modified: Mon, 16 Mar 2026 21:55:32 GMT  
		Size: 53.1 MB (53118350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57dcd2e20d0ba59a0ceda7d174daf8edc831e31e2d722a352fbe87f7cac9ae5d`  
		Last Modified: Tue, 17 Mar 2026 18:47:13 GMT  
		Size: 91.6 MB (91632901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff570b5bd4d35345136fe3a7f4b0f92660b5136d7a78252a07add026939c0790`  
		Last Modified: Tue, 17 Mar 2026 18:50:33 GMT  
		Size: 91.0 MB (90987249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a86d804ae81a1f3467f8fce0b9e74d1faa371e19a0a54b4a928141ad416754d`  
		Last Modified: Tue, 17 Mar 2026 18:50:30 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9646354984498369ef694275cff4ae186e8fb32edd3559d02f37167dbcc709b2`  
		Last Modified: Tue, 17 Mar 2026 18:50:30 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:1e18fd0f32d1df0ce441ba38a41a56c6c0ee83e10cd8103eb57e37c9e325b212
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7442953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bfda12ea8f04e798948ab48c1ce437b3568e322d3714de443f99b13665b727f`

```dockerfile
```

-	Layers:
	-	`sha256:1598f5265f1be750d6b7eaa5504fde2e0607f80583ebeb3d78a1ec9421350758`  
		Last Modified: Tue, 17 Mar 2026 18:50:30 GMT  
		Size: 7.4 MB (7426478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6360e3f27370fb58635c1577c36a55e16c7b27332cc45063b98fb555c7343a33`  
		Last Modified: Tue, 17 Mar 2026 18:50:30 GMT  
		Size: 16.5 KB (16475 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1618-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:0c45e3379dcf97d01e07855b923a25328232d08123623786c12797a4a8114b5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.0 MB (223026063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aa8ac674fce7982fa2ea5c31a102c92d3dd41b89feb13799a49db13e761459b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1773619200'
# Sun, 22 Mar 2026 19:27:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 22 Mar 2026 19:27:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sun, 22 Mar 2026 19:27:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 22 Mar 2026 19:27:56 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Sun, 22 Mar 2026 19:27:57 GMT
WORKDIR /tmp
# Sun, 22 Mar 2026 19:48:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sun, 22 Mar 2026 19:48:53 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sun, 22 Mar 2026 19:48:53 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sun, 22 Mar 2026 19:48:53 GMT
ENTRYPOINT ["entrypoint"]
# Sun, 22 Mar 2026 19:48:53 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:90acba8ac92ad141ae919a99e64549b2f417e5b2ec79f1a99dbc8efba0fea96b`  
		Last Modified: Mon, 16 Mar 2026 22:09:11 GMT  
		Size: 47.8 MB (47792328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c45c9549b3fd22069333772ff17a0ac1235b4853c85fca137130bf290f6f49b1`  
		Last Modified: Sun, 22 Mar 2026 19:33:35 GMT  
		Size: 90.8 MB (90773420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e249826f4cce91d8a894c38b01ca4d7e16a06e713f44aad175b55e8199c052`  
		Last Modified: Sun, 22 Mar 2026 19:53:06 GMT  
		Size: 84.5 MB (84459274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2e259ca44aea194ade01945666f5052c9c8b89d05631eed129b3d2e495eb74`  
		Last Modified: Sun, 22 Mar 2026 19:52:53 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0844e62782f30095faa53fcd5116d9583f81d4d4ee31ba5b0771b1db9c9357d9`  
		Last Modified: Sun, 22 Mar 2026 19:52:53 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:0c91829b31f3fea119b02b02bc7857017c2d1ca94a4a347ab0aed15d76429002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7425146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1591ee5f0edc923842a7a6c73244f919358f4eba786a011e1d2cc195c3de89f8`

```dockerfile
```

-	Layers:
	-	`sha256:0e75635d7d827a9c428da5edf1f1787f0ce7717fee283e30f8679211c53a9093`  
		Last Modified: Sun, 22 Mar 2026 19:52:55 GMT  
		Size: 7.4 MB (7408671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42c4500d5d2bebb0e29e3eb95d9abdb33015431d32b9161ad5c38757e0ee22d1`  
		Last Modified: Sun, 22 Mar 2026 19:52:52 GMT  
		Size: 16.5 KB (16475 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1618-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:ddfcc3ea2ac31b18992aa2c31daaa3eb274294d3b94149f97537dd6f33433ac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.1 MB (224144877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f6aa2d6a3a0dedf5149362b73d3ede1f38f4effc59026f31c13e50aef210f47`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 11:46:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 11:46:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 11:46:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 11:46:37 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 11:46:37 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 11:47:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 11:47:24 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 11:47:25 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 11:47:25 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 11:47:25 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7bc76783a6155f9347e92234e4b5c38bd02638c6de782f4623d0736c769250f0`  
		Last Modified: Mon, 16 Mar 2026 21:52:57 GMT  
		Size: 49.4 MB (49364775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe9cc4d4313bcb67831a520ec3cbea4454b8d7e2e5857c4b81c8882a9f9169d`  
		Last Modified: Tue, 17 Mar 2026 11:48:06 GMT  
		Size: 88.2 MB (88233869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:069f6120ba7bd911b18592da954360721d22964c2a9bf8560033ae7e012c37e4`  
		Last Modified: Tue, 17 Mar 2026 11:48:06 GMT  
		Size: 86.5 MB (86545192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4dcb3d4f8cb5ac00ed25655e5d7a7b60f284790098e68b1514cfcf783eb1ff`  
		Last Modified: Tue, 17 Mar 2026 11:48:04 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee0ec3d145962276a38abfa0ff97902b67109f2ebdc581f97c73f7878e0497cb`  
		Last Modified: Tue, 17 Mar 2026 11:48:04 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:938064adc105c03d50179af9e201fabc6805d2b7681f4d5c83f75726ceeb324a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7435631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fda1baf27fb3e15034e09fdc816066ebd5c15ba280f0733ca032ff79d5438a3`

```dockerfile
```

-	Layers:
	-	`sha256:9e8ad3687e826794f5034d539f93491c6c40df4b59d0e582cc3d7eeb24619793`  
		Last Modified: Tue, 17 Mar 2026 11:48:04 GMT  
		Size: 7.4 MB (7419217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0efc8a019c466b55cdd8379bf31390526bd6a80d9449b8fbbbf5d2eda7fce766`  
		Last Modified: Tue, 17 Mar 2026 11:48:04 GMT  
		Size: 16.4 KB (16414 bytes)  
		MIME: application/vnd.in-toto+json
