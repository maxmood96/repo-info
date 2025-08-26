## `clojure:temurin-24-trixie`

```console
$ docker pull clojure@sha256:c57f9293b81a781a22e73f1cb4e52b2658efac5c4c10abf9be2dcda04fa2be9a
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

### `clojure:temurin-24-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:91e816646a2f71eb10cb2f2f78fb70453fbeb630d30db054728a91ae9a878d9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.8 MB (224787358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7059b67699c2e6b0d9b4683e84b4ac44357951a4767c63e5db611cf813b910b1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:80b7316254b3093eb3c7ac44bb6c34bde013f27947c1ed8d8afe456b957ebfdb`  
		Last Modified: Tue, 12 Aug 2025 20:45:14 GMT  
		Size: 49.3 MB (49278280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0884f5f9a14686d41242b06d9b572a502db9a1e13703a15e16c68bb54cb018bf`  
		Last Modified: Tue, 26 Aug 2025 17:27:48 GMT  
		Size: 90.0 MB (89975190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2f85f490c90979c69efd8d470b1f502c44384b8bdd5cb372641eb2ef5a8481`  
		Last Modified: Tue, 26 Aug 2025 17:27:48 GMT  
		Size: 85.5 MB (85532844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7b54e014dfee69fdcefdfc76187d90a8d20dd8a91899446a2023ee0c8a241d`  
		Last Modified: Tue, 26 Aug 2025 17:36:50 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8dfe227732b1ebf2ed90e57e8ed8b727bad6a6b6f01ce22169d42b8a775413e`  
		Last Modified: Tue, 26 Aug 2025 17:36:54 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:58134c6f2539e29b3d7afda83a5e30a1851f5177e0685ea864a78f67b385cd7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7428659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea2ec0eddbd34cac2596cea198d3eab22ea937a331005fdca8b0d6e7a6367d90`

```dockerfile
```

-	Layers:
	-	`sha256:b3b1eb61223190f2402074501e20137978f1bb4759c5256ba64a667dc1caa421`  
		Last Modified: Tue, 26 Aug 2025 18:42:59 GMT  
		Size: 7.4 MB (7412869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7dd997a2e9c43c1ef06fbe43ef6b39ae5be970c27df5597f21ac091bdd4acd9`  
		Last Modified: Tue, 26 Aug 2025 18:42:59 GMT  
		Size: 15.8 KB (15790 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3f690acb4fc41380bde28f39606e5599304229108161238a4c0ca6ae6359d7df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.1 MB (224091832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0b602c8b10870689ec8bc0857c402a0d6b41ff7cd6ed166e03cf417a9966857`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d1e40442030765a3ac5d135c39154d052eba20953ea0e5d35a066f7722cdd93d`  
		Last Modified: Tue, 12 Aug 2025 22:12:36 GMT  
		Size: 49.6 MB (49641603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3eb89d12affa8d8ae917d4a7451665386ed8fa42334a8c26fd85c84363bf134`  
		Last Modified: Mon, 18 Aug 2025 17:24:18 GMT  
		Size: 89.1 MB (89092502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:239940211b6e0a61f3d1ba2160aa0844f82945c8e74687fa976a15d9289adbb9`  
		Last Modified: Tue, 26 Aug 2025 17:58:28 GMT  
		Size: 85.4 MB (85356681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22fc8c06b775a79516b7b549b1fda72712625ad83aa974aac4f916698480763d`  
		Last Modified: Tue, 26 Aug 2025 17:58:11 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb583f445e720acf6dfd30df140db69378b93c8d28705bc8b4ec0912edf44c7`  
		Last Modified: Tue, 26 Aug 2025 17:58:10 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:c0f2fa1048ca886b6381ee033a730eb1b399e81ae157759353221d61a9c9a9c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7435804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5112b232795a42dbd94cdca1433b426df57aed5b2f0f6e9b646cd8c88b25ad7d`

```dockerfile
```

-	Layers:
	-	`sha256:e8d5c5c247130d95f4c7636bd9a7abcf3e7717c864389739ca4c2a8f7e107f14`  
		Last Modified: Tue, 26 Aug 2025 18:43:06 GMT  
		Size: 7.4 MB (7419896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1008312253f71136f85b59ab8bec6f771e4a939525fc50324558750035ed1ff5`  
		Last Modified: Tue, 26 Aug 2025 18:43:07 GMT  
		Size: 15.9 KB (15908 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:796e02ca498542c8921a7482bcc625dd6cfadf07231edd5cb27a0dc889532ff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233863326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53308efdbab9668deb0b32a67db7d44f9c954eb7bed47100f6f5c0711d78b4e0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:befe77620590f63939f5bcadadc9f45832981822c9c901f057eb4e86f733c29a`  
		Last Modified: Wed, 13 Aug 2025 00:32:04 GMT  
		Size: 53.1 MB (53103384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a529d6ce1cfbf7646307577f9dff0071c9dbed24a6448f852c9d01fc20271a0`  
		Last Modified: Mon, 18 Aug 2025 17:40:19 GMT  
		Size: 89.9 MB (89918259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c396f8f2bec2c4a676a06f6a56965a70d1b09f9e654b130c5b90cc9169fec65a`  
		Last Modified: Mon, 18 Aug 2025 17:40:23 GMT  
		Size: 90.8 MB (90840641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dcb1c8b057ad4a5438947a28e602698a022a8fcbaf164aa333f2afe0b51a53f`  
		Last Modified: Mon, 18 Aug 2025 17:40:09 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d07d40b28876c2b1ca7fc4d378e73373e3cb0052fc177deac4b961dc610980eb`  
		Last Modified: Mon, 18 Aug 2025 17:40:09 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:2e90eab795486e932bcec4e38157de7de1e780cde9be55a4d76c849e8d9bf8b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7434424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b251be5ed2331fcbaa94117532decf06a68c19b0078954d179865491bf6dee2`

```dockerfile
```

-	Layers:
	-	`sha256:b15f4693e879b4e65ac46b1dfb8846459eb115da4d10e62edbdd9405a183b279`  
		Last Modified: Mon, 18 Aug 2025 18:44:00 GMT  
		Size: 7.4 MB (7418586 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7008cfabdb52cd23b4c96dc425a64513c432bc03517b181771deea013dfcf7b`  
		Last Modified: Mon, 18 Aug 2025 18:44:01 GMT  
		Size: 15.8 KB (15838 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:57a96c9203fa55826cfd3f3d9ddef87980b29bd4c6b45a60e5076a13d8556765
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.8 MB (219760916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:367ac4687a6ea6796430e88ca8733bca57a636d68f926764b0673dd1c037f7cc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:59f3e0adb655cb03f7d489f3cc57e302e249916bbb076c78008f9329238bfb20`  
		Last Modified: Wed, 13 Aug 2025 01:13:55 GMT  
		Size: 47.8 MB (47764303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d3c2b6d6d08922e7d9501bfee1be5dc23cd7a0ba7350b50e7d2e85a3bb3a6fe`  
		Last Modified: Fri, 22 Aug 2025 01:13:06 GMT  
		Size: 87.7 MB (87670398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a3e361a1b825723f158066b69610e428946d264c51a9ee6f3a3fcf0fc28b1a`  
		Last Modified: Fri, 22 Aug 2025 01:13:06 GMT  
		Size: 84.3 MB (84325170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c878dd86e19f678e25289e0923a62caf65e4392c8317cb8f6cfef273f31b540e`  
		Last Modified: Fri, 22 Aug 2025 01:12:54 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd6b27d7397d4b5f4541414ee954147f21b5320b8650d2a56182afd7236367cd`  
		Last Modified: Fri, 22 Aug 2025 01:12:54 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:1a5d56d3479db952210c8d4f10a5579b007db3b2ed265bfa01c0d939f038469f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7416617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:450b898008fbd9cf1078080f7d75b7e581ca99bfc45e0fed773f730309a13550`

```dockerfile
```

-	Layers:
	-	`sha256:706fcd1c32fc5e5b1861a68d413846478146613b5edd55ec4aa85044170ba29c`  
		Last Modified: Fri, 22 Aug 2025 03:37:44 GMT  
		Size: 7.4 MB (7400779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37cb9174bc9b1d222697f13b21a45576fdcd6dfdf7be2caccb1ee2871aaebb4d`  
		Last Modified: Fri, 22 Aug 2025 03:37:45 GMT  
		Size: 15.8 KB (15838 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:3d0353a7f5ed940da67ff53c4758e76ce384caf0604b0b9f5e43bb15709ecc65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.0 MB (220976720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5b3ac278d6a328a9d0671b6d31a3d98819060e30da5ae1ee74ba1b7eb43d1ba`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c3b791adea90b39bc59919a9959b7f44f65aa3364a03dd0271a5ff658488877f`  
		Last Modified: Tue, 12 Aug 2025 20:59:03 GMT  
		Size: 49.3 MB (49345161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c850ecedf25d70fc1070e9bc8d02ff404d52931fb1c7f11dbf72f9adc7e94a84`  
		Last Modified: Mon, 18 Aug 2025 18:23:55 GMT  
		Size: 85.2 MB (85226411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0afadace29cf5f56c17c325e7536b76b76abe268020a364c51c3dca96ed2ccb8`  
		Last Modified: Mon, 18 Aug 2025 18:23:53 GMT  
		Size: 86.4 MB (86404103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f890933d1d3855d47e4649ebe6ffa916f39d60926a100281c9442a48b89bfe59`  
		Last Modified: Mon, 18 Aug 2025 18:23:43 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11129af5940006c98ee5ae2cdeeef1fbdb486dc8a2347b0c556fbbb604b6c631`  
		Last Modified: Mon, 18 Aug 2025 18:23:43 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f3be6b1ece5e81e2958583753dbb41bbbe41141352420608f7d45b336587b08f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7427129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aea4c49637fcd70223f7906ef76de7536f938acd6644a8e78a81b94076343dfd`

```dockerfile
```

-	Layers:
	-	`sha256:0d5b5c88690ae9c02045dada74f6a752354f99a8a974865b420105a7202c6f70`  
		Last Modified: Mon, 18 Aug 2025 21:37:00 GMT  
		Size: 7.4 MB (7411339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4de5dd068cb6aaaaabaf06dc29398cc28c9e00ace1a81da859d137265afa5e6`  
		Last Modified: Mon, 18 Aug 2025 21:37:01 GMT  
		Size: 15.8 KB (15790 bytes)  
		MIME: application/vnd.in-toto+json
