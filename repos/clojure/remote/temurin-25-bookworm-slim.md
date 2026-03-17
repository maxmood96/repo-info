## `clojure:temurin-25-bookworm-slim`

```console
$ docker pull clojure@sha256:df461f94fa91dfeaf1bf0d8092d76a05bdc08f7cd33e67ab57d6f051be79aa75
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

### `clojure:temurin-25-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e0c89d927da956c9a0889950fc02c8db2850e6a370b7c3dcddd8f12e0ecbed48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.2 MB (190194842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c83bf6848f1e338ea7d84aed56ca5e0684c1f5bdb539fb140e22057226947b0b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 03:01:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 03:01:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 03:01:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:01:15 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 03:01:15 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:01:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 03:01:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 03:01:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 03:01:29 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 03:01:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db5e59d0d8c1dc65c48ff836980376558dffb4589730ea45f73d65cd37dd389`  
		Last Modified: Tue, 17 Mar 2026 03:01:50 GMT  
		Size: 92.3 MB (92256282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3ec1c5b7f8f6712c0747d866557a5d08f22fb1d7c33f3d1e9d411a43753a903`  
		Last Modified: Tue, 17 Mar 2026 03:01:50 GMT  
		Size: 69.7 MB (69701292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8422d91bf3284781f0fd52e76cac315d902ed197f99c7e637c6e1f7aca16d1ab`  
		Last Modified: Tue, 17 Mar 2026 03:01:47 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e1a21823163cd2eb98ce5e5d60a87438d3c164ac2d149e3a9df226b11d7c09`  
		Last Modified: Tue, 17 Mar 2026 03:01:46 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b50088fea6167a665c9204d683bb1cb3bc27bee7f8e5b5a5405a4dec0da22c26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5100786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7c9868f506b19fa344c3e468d57c8c12c0723866116ae3be159ab08d1860a34`

```dockerfile
```

-	Layers:
	-	`sha256:13bb6b2c6ebbaf2879f87f0d3f4e6a85a1c273bc19fb336a118e773cc8c2de47`  
		Last Modified: Tue, 17 Mar 2026 03:01:47 GMT  
		Size: 5.1 MB (5084261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f893f36f0e34e3c808e353054db61f460c97bcbbb6e96969e479d100ce6cd22a`  
		Last Modified: Tue, 17 Mar 2026 03:01:46 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f69186db98ff11e7791ef9ae4e679c54795290564281cb5f5e6cdc0c1589aef1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.1 MB (189094299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b01788d3537b3605f51256aee00be887f44e2e48bb1dc742c566eb00b0990124`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 03:05:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 03:05:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 03:05:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:05:30 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 03:05:30 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:05:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 03:05:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 03:05:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 03:05:45 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 03:05:45 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6739b0fddc67e48ae563159c66e89e94443f8694e22de38884ea27933e354da3`  
		Last Modified: Tue, 17 Mar 2026 03:06:06 GMT  
		Size: 91.3 MB (91288265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:664560654a76bf1be80265f0768269d15b8cf6e4aca558fb3294bbb7df3167ce`  
		Last Modified: Tue, 17 Mar 2026 03:06:06 GMT  
		Size: 69.7 MB (69688930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6081d6d3c06507c67c783520ed9754cc32fd8a0183a4435f24e6004d82c14d51`  
		Last Modified: Tue, 17 Mar 2026 03:06:03 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9d8e216902047818a2150e0ccdb8051105923e2ee6bf99f1a50317769eb5fc`  
		Last Modified: Tue, 17 Mar 2026 03:06:03 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7861cc38723d106f4fdf42b9367a470d91970c949f0f12255f510e647f6e31c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5106710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2251d1e6a2ee987a881c92c0f7e48539af7c41523363fbbd239c15569739588b`

```dockerfile
```

-	Layers:
	-	`sha256:919820755a0aceaa2b308579ab3fd5371f50cdd35a9a1a97980cbaf4c627c1a6`  
		Last Modified: Tue, 17 Mar 2026 03:06:03 GMT  
		Size: 5.1 MB (5090043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3875bfdc0048553158221a6706e9344e1338b96cec73075c1e1cb9209f8feea`  
		Last Modified: Tue, 17 Mar 2026 03:06:03 GMT  
		Size: 16.7 KB (16667 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:bdd102d9b05273f1ae4dc79116ea18bc93e08b4809681377757fde895c28f049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.2 MB (199245812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a975a3481257753a521e0c340671e6a6ecf0cdce3c485fa61f5413c4be9c966b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 18:44:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 18:44:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 18:44:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:44:27 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 18:44:28 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 18:48:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 18:48:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 18:48:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 18:48:23 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 18:48:23 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7a0392d98c02d4219c67a8e3d3837c1ac5d4af6836b9264bdd6c427cc7a24f76`  
		Last Modified: Mon, 16 Mar 2026 21:51:26 GMT  
		Size: 32.1 MB (32078368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4315bac4f2fd5b7cb762fb218c4aa27e365d21f64f79e49d816da2b15b8cae7`  
		Last Modified: Tue, 17 Mar 2026 18:45:39 GMT  
		Size: 91.6 MB (91632917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bff431448a001c7f4677b0b01bc0dd6d11432006a0a1613e6e64c44fec28875`  
		Last Modified: Tue, 17 Mar 2026 18:48:55 GMT  
		Size: 75.5 MB (75533486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62eaf47e5339bca4422f4cd5347f3cfcf27506bccfce271f2b128f56f720937`  
		Last Modified: Tue, 17 Mar 2026 18:48:53 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00fb0a558d424cbee96d2d5779b5df2f30b89f99f3fe03dd222b40230c0fb94e`  
		Last Modified: Tue, 17 Mar 2026 18:48:53 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bef5fcf553182333f6d069f724bdefe070b64c1781d88e92ff4fb54da5ecde20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5089328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d08017d50771667bca4fdb800c8d5837a989f066e87000efc91a02d5b22f565`

```dockerfile
```

-	Layers:
	-	`sha256:e2bff139d9a96493f5c2290248c428551bd43cd3309b6464b56a525d2a85f74f`  
		Last Modified: Tue, 17 Mar 2026 18:48:54 GMT  
		Size: 5.1 MB (5072743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e22f53695d7ce4d07f68f2cabbcde76c16d79d1e8a989250b3ed24a2b4a7ba1b`  
		Last Modified: Tue, 17 Mar 2026 18:48:53 GMT  
		Size: 16.6 KB (16585 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:4204524fa8b3bf86af0057535a3ed07bb91c3306d48bd27195f0bea49e164cb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.6 MB (183640617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed6d4d6569a6f62d7ca1c2b397ec3eca86d872295f8aa0799837c60693ac28a2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 11:42:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 11:42:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 11:42:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 11:42:59 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 11:43:00 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 11:45:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 11:45:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 11:45:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 11:45:46 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 11:45:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3814d1a754476ec8db22d31a68bf8b939774ab72a69dcd1b72cff2f3b9a06022`  
		Last Modified: Mon, 16 Mar 2026 21:51:33 GMT  
		Size: 26.9 MB (26891515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b3b8db134f694fe9a88a6d136509657f069ae40f60c275bad46fdd5792b0de`  
		Last Modified: Tue, 17 Mar 2026 11:44:03 GMT  
		Size: 88.2 MB (88233848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede8d0b15e0dd424036f0be28c3cbae8d23ec1714fc8d350137c1093f77058d7`  
		Last Modified: Tue, 17 Mar 2026 11:46:18 GMT  
		Size: 68.5 MB (68514212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045bc38690eadcf972a95d7d531511b1b91ce8642836563f20665fdc71ac95c7`  
		Last Modified: Tue, 17 Mar 2026 11:46:16 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8134c13246b28e7bb64b3c8fdfb61a6faf874258a449902874adb3e1153d1a9a`  
		Last Modified: Tue, 17 Mar 2026 11:46:16 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e5f8f5c95eb95304b3b7746b6b15f4592423c5f3b39b505acb3af225985bc141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5076669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd865867252dfedefef57c98504a50a3b9cf56723af1fa49302d82ddc3cb0b02`

```dockerfile
```

-	Layers:
	-	`sha256:c4f41eb47d6747d58d8da778e6bfdd551378562cc5c3e87a02356eb49c1169c7`  
		Last Modified: Tue, 17 Mar 2026 11:46:16 GMT  
		Size: 5.1 MB (5060144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45de1d075f714cfdde61131b6b44b526547d33273e4173b41ed97913f6ca3ce5`  
		Last Modified: Tue, 17 Mar 2026 11:46:16 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json
