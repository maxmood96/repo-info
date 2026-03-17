## `clojure:temurin-17-tools-deps-1.12.4.1618-trixie`

```console
$ docker pull clojure@sha256:b0b56f6ad397a21fb19a494078c716ed8d8932868128c563feaf90dfaf2a31c2
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
$ docker pull clojure@sha256:cac6b8c81a59b65c7fb99116b8103490923a50fb3043794938e644735b7b0537
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.5 MB (280494230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acb5041252c4bbb1c99fcd938cf598d67c72badbde1f9f8421b567f0590bab96`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 02:58:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:58:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:58:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:58:44 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 02:58:44 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 02:59:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 02:59:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 02:59:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 02:59:01 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 02:59:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8f6ad858d0a46fa8ee628532c70b8dc82d06179d543b0b09ec19fc03d4c5b373`  
		Last Modified: Mon, 16 Mar 2026 21:53:17 GMT  
		Size: 49.3 MB (49297530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94abf4187070857e834be97b2bead1c38b1a3c811318510c69725cb686ba9f7f`  
		Last Modified: Tue, 17 Mar 2026 02:59:26 GMT  
		Size: 145.6 MB (145628435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa2dd57aa48f7fe671b969de6c98b0d21e2b4c84b8e7eb009819d49e4b42575`  
		Last Modified: Tue, 17 Mar 2026 02:59:23 GMT  
		Size: 85.6 MB (85567227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e459819902b395adbd86adbb59c597b6f6d51f7ad42aae4106215f666008da50`  
		Last Modified: Tue, 17 Mar 2026 02:59:20 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696afd42beb05a4c6644a3501bb10b460f75fdc3cc4d15f5a50e2cf7b7b15a78`  
		Last Modified: Tue, 17 Mar 2026 02:59:20 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:af3632df23a205103627abe198b72640705e992960752e4005175a04ba85fdb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7486421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b13c03e0fca502c0cf1942d4121c04dd588a1d632719817e6b91b39bcf1e685b`

```dockerfile
```

-	Layers:
	-	`sha256:55ff943ebc9d7132be9d7954564f5daa0cb77a5760d1f0468c96efe5a49f4778`  
		Last Modified: Tue, 17 Mar 2026 02:59:20 GMT  
		Size: 7.5 MB (7470667 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebb06e7ab519f62e788c23801da1ed68cc69ad7dbb1f96430f725b9658f71ba0`  
		Last Modified: Tue, 17 Mar 2026 02:59:20 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7a12f4abe6c5f1bfe30978b7462bb736c8e3a72fdc53d0b529ba99a83445af42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.5 MB (279485421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83393bea52a34bf00881d30fd7096fc5901fc938dbe2e11b71e94b4609c0d5ae`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 03:03:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 03:03:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 03:03:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:03:29 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 03:03:29 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:03:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 03:03:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 03:03:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 03:03:48 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 03:03:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:deab8db42772fcfeb45003461fe0eb7bf63bdb29199a4fb76242b9493437c28b`  
		Last Modified: Mon, 16 Mar 2026 21:53:03 GMT  
		Size: 49.7 MB (49664953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc4d20db6a99cecac94193b1848be4ed2d9a1630ea0fe32bdf8ab2ee66497bb`  
		Last Modified: Tue, 17 Mar 2026 03:04:13 GMT  
		Size: 144.4 MB (144436241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e9ea94e394271119478116dff787271fe37dee113b82f89f30476d137f9f160`  
		Last Modified: Tue, 17 Mar 2026 03:04:12 GMT  
		Size: 85.4 MB (85383186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c59d196d85255586fa2917637592f591d043fcf526e63820486abdc852025b4`  
		Last Modified: Tue, 17 Mar 2026 03:04:09 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e770d00dfb7ea79b8b91a3e5132cd49232479022299073cc1130f73c33c6c7`  
		Last Modified: Tue, 17 Mar 2026 03:04:09 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e279198814f72a34e603ccbc353965ad6eb7f7ec7f62c6987bc90c4d94353db8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7493569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16507af1823a277744bfe0a7bed3d076b9e9c6a4c1b1bc7fd1077ad55018542d`

```dockerfile
```

-	Layers:
	-	`sha256:1362eb6235b00f001e27bc785039b6241825a32581fd50d310ad08cbeba6d4a7`  
		Last Modified: Tue, 17 Mar 2026 03:04:09 GMT  
		Size: 7.5 MB (7477697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4eb712feb0032c60412e09bc47d4eb8d45d131847b93d339437fb73d115800b8`  
		Last Modified: Tue, 17 Mar 2026 03:04:09 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:bddb9df7df87ef95ac3459235d08ae129926b3c5cc3ccc48b7cdadee1276358c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.5 MB (289528095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:528d55849a428d77a6f0c6cd80a2fffd5ffb7d2b8dcf32e24300f338b5d1383c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 20:54:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:54:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:54:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:54:24 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:54:26 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:55:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:55:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:55:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 20:55:33 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 20:55:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:468eb7cd0e9ceb9e5b1c4c9daadd36c2fd1f1ee82c667dc1a7d70fa95600a20f`  
		Last Modified: Tue, 24 Feb 2026 18:45:11 GMT  
		Size: 53.1 MB (53112261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa68eefccf52feae213c365bd35426d2716c52016a1ead8472aed0ffcacc64c0`  
		Last Modified: Mon, 09 Mar 2026 20:56:25 GMT  
		Size: 145.4 MB (145438177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd88027fdb0a73e7821484ecb535361a5f5a05f0f77ab8f269390b8349b7024`  
		Last Modified: Mon, 09 Mar 2026 20:56:25 GMT  
		Size: 91.0 MB (90976614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2f0af1a45089a1861b447771d51340708e3fb00682d26d1679459aad59944e`  
		Last Modified: Mon, 09 Mar 2026 20:56:21 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ea1779e7a8784a0b84029276a56471700b7e9d7250bc5a946cbe09d448e412`  
		Last Modified: Mon, 09 Mar 2026 20:56:21 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:089a6806c7dd4b1a94e1544b527ba134624b04fb5e6c8128ad0da744143897cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7490816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2776756d3c79627afe612b34d6bd69606ec9d77e37fb21e2ad75eab888037ec`

```dockerfile
```

-	Layers:
	-	`sha256:be74f7e5ab538f7814c096a584e9e1ecdcffd9d79402faf51c579d71829b4c15`  
		Last Modified: Mon, 09 Mar 2026 20:56:21 GMT  
		Size: 7.5 MB (7475014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d7d3f0f4a7b6327f92112d5b7f0369643998bab5395078edf1fa762f4424b00`  
		Last Modified: Mon, 09 Mar 2026 20:56:21 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:b1839b7469cbd8d62594e226d6cfdbb8f28c254dfbdbe0b297dfa9ef5a5e08e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.9 MB (274892990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:805fdd8d258b91177101c9390cfdf85c2fe412a09ac7731c3a2d463e17dc2cb1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Wed, 04 Mar 2026 10:51:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 10:51:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 10:51:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 10:51:35 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 04 Mar 2026 10:51:35 GMT
WORKDIR /tmp
# Tue, 10 Mar 2026 01:13:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 10 Mar 2026 01:13:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 10 Mar 2026 01:13:40 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 10 Mar 2026 01:13:40 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 10 Mar 2026 01:13:40 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3be247472b67578a1d05739722d8adeca41098796e5d6210800176db58046fa7`  
		Last Modified: Tue, 24 Feb 2026 18:57:42 GMT  
		Size: 47.8 MB (47776936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db99fe8e9aa791e3b0fe2b096e079a262bb09902b5d09c2085e34c6f29398e4a`  
		Last Modified: Wed, 04 Mar 2026 10:59:51 GMT  
		Size: 142.7 MB (142662998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2bd222e0edd4ebafc8c5ac11fcb679d7a6f73548444c3b3e9940bb59604385`  
		Last Modified: Tue, 10 Mar 2026 01:18:59 GMT  
		Size: 84.5 MB (84452009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4885ee0056533d9c795513a48e2be1d581b2d84cb39f3ca05f990d26965a36c`  
		Last Modified: Tue, 10 Mar 2026 01:18:44 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8068b91f93b5e43639679cc5faa09af9c05c368b0a816dbb769730da36ea35`  
		Last Modified: Tue, 10 Mar 2026 01:18:44 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:9d7dd84d184cd6f0ad9f8f05eb685cf294a79614b230dd8f860f163f6284d634
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7472391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5638f259123ab01a238d17a784bf52d7201038a305672a086dc5c530b3c39533`

```dockerfile
```

-	Layers:
	-	`sha256:449afb46952dd734653cf626a966e8e2589a85de04a2d2d2e2d3914ac0367fb4`  
		Last Modified: Tue, 10 Mar 2026 01:18:46 GMT  
		Size: 7.5 MB (7456589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ccfbceeaeb59dffe29778e6392dad3cf6e3e61225b8cbad4ae3fcb721412ef6`  
		Last Modified: Tue, 10 Mar 2026 01:18:44 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:f08f1e7f6961a3d36c78353491dfab3500f90988aec0a125faa8dddc093d527e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.5 MB (271537398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e0f4a01498f87338919c6429f9cb8782a410b3476bd6fd297a4caa2f0164cd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 11:38:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 11:38:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 11:38:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 11:38:14 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 11:38:14 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 11:38:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 11:38:49 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 11:38:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 11:38:49 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 11:38:49 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7bc76783a6155f9347e92234e4b5c38bd02638c6de782f4623d0736c769250f0`  
		Last Modified: Mon, 16 Mar 2026 21:52:57 GMT  
		Size: 49.4 MB (49364775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0e873883d06c3d66937d1b59b9c75c3451b6c0508819963b4679d67d56b74c`  
		Last Modified: Tue, 17 Mar 2026 11:39:29 GMT  
		Size: 135.6 MB (135626794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dce659ad6837cfd9848b82516620de7a17b108d78fe5d71af59ff45354e5c47`  
		Last Modified: Tue, 17 Mar 2026 11:39:30 GMT  
		Size: 86.5 MB (86544786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc002232db3caef7cd659f3fe252614c9e3a5e36e397ccf750585dc0ec2e233`  
		Last Modified: Tue, 17 Mar 2026 11:39:28 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526b39e47290645406fdeffe5e9d97c15fe22f0cdb2b7a006a3a4ebdffc90290`  
		Last Modified: Tue, 17 Mar 2026 11:39:28 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:ebfff3dba69fbd4d7fb95b91b2f5a04bec022353009e76a2e923825589f29240
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7482343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2e6409197409b7313ebd627012a931fde9c375d85bd5a5b4da6fedfc39e0f28`

```dockerfile
```

-	Layers:
	-	`sha256:99407ea26d8c5fcb25d38e1c1418fbfe85dce72a15d001cfcb61c444ada3ebfa`  
		Last Modified: Tue, 17 Mar 2026 11:39:29 GMT  
		Size: 7.5 MB (7466589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0dead34be928309ca50553e17468adafaa452df070981c625c55aee613b19abf`  
		Last Modified: Tue, 17 Mar 2026 11:39:28 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json
