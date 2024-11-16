## `clojure:temurin-8-tools-deps-1.12.0.1479-bullseye`

```console
$ docker pull clojure@sha256:323cb268c3f8617cb10587fc4fbd617579c23c93260591efe1097fc22277fabb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.0.1479-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:e0f85b90ab3322ba0a2d221ca1853d27da58c4ebccccc27159a28fd99a6c7833
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227882022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:411ab175d3fcadd83d6747a4029214bca13e6bdd8dd8da763bee564982be0ca7`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c2056d933cd629f55ac55802dda223f122286bf60ec42a24f0d0f6ae2615315c`  
		Last Modified: Tue, 12 Nov 2024 00:55:16 GMT  
		Size: 55.1 MB (55108780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e80a6c89f000203491439ab3b5dc3d04897c5098da197a49923d410c94d5a1`  
		Last Modified: Sat, 16 Nov 2024 03:51:34 GMT  
		Size: 103.6 MB (103633935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e251ec0078cc8ddae531790e3e35f2a161fd2cef0ba49d588a36fedbe613a4e`  
		Last Modified: Sat, 16 Nov 2024 03:51:33 GMT  
		Size: 69.1 MB (69138663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e8917b5500fcbf60b84ab48233811c3bb19d36cd3691e23832d1d54cbfe5b3`  
		Last Modified: Sat, 16 Nov 2024 03:51:32 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1479-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:0b4cf824ddfeb1bae122a88087b4c63b72c8ccc973ef2b0458dffe31550e1e03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7352282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:863843c381ea00295278f52f09e4968303112e195af2b40494b13564dac62a61`

```dockerfile
```

-	Layers:
	-	`sha256:473866c42cd490edbcdab02d5f1e488ebb3a376205d214cafac2eec57680a7f2`  
		Last Modified: Sat, 16 Nov 2024 03:51:33 GMT  
		Size: 7.3 MB (7338040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6f5d2f8c3da9b604a242e125613604c0a53ddd7037e166ee0e8daf76a8afba4`  
		Last Modified: Sat, 16 Nov 2024 03:51:32 GMT  
		Size: 14.2 KB (14242 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.0.1479-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f4ae0fa6d232e71b7e5a101537a07b06d0acc1a8d35ce05d07a8c4022578c1ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.8 MB (225781698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:038a742611895c321db63ba6e261f5879377ad486f5a59d80c7d495156587000`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:a839664fe62f615da74af799f94ccbc890a15d0f78470aac54302c2fd5475615`  
		Last Modified: Tue, 12 Nov 2024 00:57:41 GMT  
		Size: 53.8 MB (53757072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feefd6a247880c6e3044381c4f7978a1eb973d63cd6342d8f7beb5de7f84e18c`  
		Last Modified: Sat, 16 Nov 2024 05:13:03 GMT  
		Size: 102.7 MB (102747729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a53de83d3262242e720cd2d0fdd5bbfcaf635dc8ee55bc1751fa62233b763f9`  
		Last Modified: Sat, 16 Nov 2024 05:17:27 GMT  
		Size: 69.3 MB (69276256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34be34dc4cce404d2b7b8187c0ec9b0517575066df4ff952ab337ad42c4ca156`  
		Last Modified: Sat, 16 Nov 2024 05:17:24 GMT  
		Size: 609.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1479-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:8e1e47cf222e94261003df7aa5d9047db02d0847edf5eb90bbc2bb130556b37f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7358201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7733a98d5d31c00bdc63a7ad0257f6db266bce525b79582d1e0c5ec5b50e5bd0`

```dockerfile
```

-	Layers:
	-	`sha256:c0167716a68fd8ad892b5fe8a4a9f50c4f4bf2de7f3235604df890d6e3582292`  
		Last Modified: Sat, 16 Nov 2024 05:17:25 GMT  
		Size: 7.3 MB (7343842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a14cad80392f5af9b4d09e0067f6b63b8f48f4949b9b3b778841c368764753d3`  
		Last Modified: Sat, 16 Nov 2024 05:17:24 GMT  
		Size: 14.4 KB (14359 bytes)  
		MIME: application/vnd.in-toto+json
