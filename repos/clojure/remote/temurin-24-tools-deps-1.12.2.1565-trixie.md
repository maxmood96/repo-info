## `clojure:temurin-24-tools-deps-1.12.2.1565-trixie`

```console
$ docker pull clojure@sha256:7bfb5dbf29108d30d40acd4c81767f0a24ad28eab555655d2b7e2d881ccfb7f1
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

### `clojure:temurin-24-tools-deps-1.12.2.1565-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:7e36a082a0669d6a86da4cb833e3a84d261edd4620a17fbc2bf098ad312badb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.8 MB (224787446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03eb48f1c84c5d940ff076a190a02332c9d87027e22238a7f3ea6804d4ed3c10`
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
	-	`sha256:aae53c622de7e926dc1ede053a2896243ee0607a22a3027c13dd7b590c2841a4`  
		Last Modified: Tue, 02 Sep 2025 01:56:01 GMT  
		Size: 90.0 MB (89975188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1270df97560dac71d1a50717f03dc2593629ee9e96b4ba80c4f36a8d53aa15`  
		Last Modified: Tue, 02 Sep 2025 01:55:47 GMT  
		Size: 85.5 MB (85532932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44f096c716780b0d7901b07a70d8a6b137836b1bc891781c0f45b9a6ffebc11f`  
		Last Modified: Tue, 02 Sep 2025 01:00:59 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0936f1c26e11eb470a84528eb8808118898b7b0a09b00459aad3283048b2b28b`  
		Last Modified: Tue, 02 Sep 2025 01:00:59 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.2.1565-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b2714212c4b91255d962d2388f2921c7ebfb137bf822caad332d61096d307d18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7428659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b1030a5e3dedc920c8ff6daddc74e1c140d97eeb2eee072918ba93ba5a585ef`

```dockerfile
```

-	Layers:
	-	`sha256:f75eafdc9215e0f92b6b1e2fad5609d10f572e9c55f5852cb40e4f57f6f72abd`  
		Last Modified: Tue, 02 Sep 2025 03:44:48 GMT  
		Size: 7.4 MB (7412869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b55d1accd69c9f0ca57978d35e94275e3882c5b5ef8a4bc83282de483361748a`  
		Last Modified: Tue, 02 Sep 2025 03:44:49 GMT  
		Size: 15.8 KB (15790 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.2.1565-trixie` - linux; arm64 variant v8

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

### `clojure:temurin-24-tools-deps-1.12.2.1565-trixie` - unknown; unknown

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

### `clojure:temurin-24-tools-deps-1.12.2.1565-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:c8ef57f704ea876d17baad7ec10e7381276eb4d6a7f7dc7fea47d0e05bf30ca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.0 MB (233964753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8766f3ade22e6f9e09136235deb861750fb0531e6467fbede695ad6e0b14b056`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
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
	-	`sha256:abc1a22d4f127131cc1e3b3e910c0690c203c8d48f619cf619fe96c75d74a008`  
		Last Modified: Tue, 26 Aug 2025 18:21:49 GMT  
		Size: 90.9 MB (90942063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93cd95022b420674a216096a0667ac3ef586d5a6ac944a0592ac84eef91d25cb`  
		Last Modified: Tue, 26 Aug 2025 19:09:33 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b58493ae4c2afed6f9b7de46d29aa4095f515a0db2a2ac6f8fbedb1a320149`  
		Last Modified: Tue, 26 Aug 2025 19:09:33 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.2.1565-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f388d199bce4fa8966206687a0462011a3eb0f3451cf84e297a6d0d249edbc5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7434424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:605d75629cfe8abaa969dce2a3158e186ec88f78b69be98651a1efd8216534bb`

```dockerfile
```

-	Layers:
	-	`sha256:552463a052940aaf02c203a3dbc015cf53743edb79b41f171e80c2b7e11d405e`  
		Last Modified: Tue, 26 Aug 2025 21:39:02 GMT  
		Size: 7.4 MB (7418586 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af05c33742940b0b49d33bfca3ad80661328a4569c5afa71cd168cb7c92f4a33`  
		Last Modified: Tue, 26 Aug 2025 21:39:03 GMT  
		Size: 15.8 KB (15838 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.2.1565-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:c79e70adbc73f8091d61a9ea18dcaa5660efff3addb43c7d44dc82dcd9bc63aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219860606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b75d4d7c630b3a15f89f5a84b0836f4904713d9f4e4b287f91bc1ae7d91ba06`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
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
	-	`sha256:942514859d7fd3108989c807bc2961246a460ac3569de7a98fe8e4cf2216e036`  
		Last Modified: Wed, 27 Aug 2025 09:48:12 GMT  
		Size: 84.4 MB (84424866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650d9825377ed8449de282f2a5090aca3ba1a9fa18cb7bc57cd846481d2c905b`  
		Last Modified: Wed, 27 Aug 2025 09:47:51 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ae34373a9a31033a6ea6cdbf82f75a359bad1e8722a99ca240a22de5c5ed3f5`  
		Last Modified: Wed, 27 Aug 2025 09:47:51 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.2.1565-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:5eeca6392fa8462d9c77c48f48ca8283d73bc7866731123c124f1700ca3701ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7416617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:538f45d6e475e8db5777e293e470fd36822e8af3071f6124641f705c26ca1bf8`

```dockerfile
```

-	Layers:
	-	`sha256:87c1b702c57e331d9ff9578937070ad7ae926e32e7748ba73512549120a87c22`  
		Last Modified: Wed, 27 Aug 2025 12:37:35 GMT  
		Size: 7.4 MB (7400779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4875a53654ceaee620e2a463646d038f624b6402ceb37bd4bdad3c09971e2b6d`  
		Last Modified: Wed, 27 Aug 2025 12:37:36 GMT  
		Size: 15.8 KB (15838 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.2.1565-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:36e2805373d61cf426644bf36d8ac132ca5a491d5ef38abc84d7e002054b96ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 MB (221071004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f019b952773688e225621bf5ef7ea13f51f25115113984a20e14fa983a98d4df`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
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
	-	`sha256:c3b791adea90b39bc59919a9959b7f44f65aa3364a03dd0271a5ff658488877f`  
		Last Modified: Tue, 12 Aug 2025 20:59:03 GMT  
		Size: 49.3 MB (49345161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cca0edb91d03cae6270e53eeeef43feaf55bea767ca7852d2b4ff7be27bf259`  
		Last Modified: Tue, 02 Sep 2025 02:24:49 GMT  
		Size: 85.2 MB (85226361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e5c397da2c8d623c4b6a425ebcf59b73e2a8cb6fc22117194644f6b5707c2d`  
		Last Modified: Tue, 02 Sep 2025 02:29:50 GMT  
		Size: 86.5 MB (86498442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c55927a56b08de0547f3526b3cf7bb275c1efa9b4cbafd87f87c7f7fb7e4626`  
		Last Modified: Tue, 02 Sep 2025 02:29:39 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa527c947fabfb01642a54504a25554134ed99d572505b8c4b935e59649fc142`  
		Last Modified: Tue, 02 Sep 2025 02:29:39 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.2.1565-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:1a6deded8ee46c08c94403784dd25513919133433f9acb1f3e6f06a9dfbdc27b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7427129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d1e03d93842af3b1d66c4432ecdc7a551308fb5e1cee23a6b78f597dd21e1c6`

```dockerfile
```

-	Layers:
	-	`sha256:620240083ecba74e5d1d4ba23df0ba0621b11068c934f021312eb5857ef2254b`  
		Last Modified: Tue, 02 Sep 2025 03:45:11 GMT  
		Size: 7.4 MB (7411339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53709ae8ad0914f691bb2e6f3c2d4c45a0e768bc4df9c1887e83c60a474d3de5`  
		Last Modified: Tue, 02 Sep 2025 03:45:12 GMT  
		Size: 15.8 KB (15790 bytes)  
		MIME: application/vnd.in-toto+json
