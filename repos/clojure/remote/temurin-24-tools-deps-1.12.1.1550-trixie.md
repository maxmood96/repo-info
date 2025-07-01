## `clojure:temurin-24-tools-deps-1.12.1.1550-trixie`

```console
$ docker pull clojure@sha256:e97ea9ad7ff9ab68b9d8432be1e108ea278438f37fb41d5bac1a271bc839fa31
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

### `clojure:temurin-24-tools-deps-1.12.1.1550-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:78a22b9ab573a7f472589fcbfb373f5dd1f81561b50c6da0b0237ec5650b07b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.6 MB (224572075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cd3d53c9e36c02868c7a5eead04b0d63937ebefc2bc3a781c64d1dedea78345`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b72fed6e2775feec9291a4bd4b416f996dfc503eda11eaa00def55711302b4ce`  
		Last Modified: Tue, 01 Jul 2025 01:15:00 GMT  
		Size: 49.3 MB (49263877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28212f83f34f9187a39f19356f9f8ae4deae3d468f3f2e1bc726a41415c0a33c`  
		Last Modified: Tue, 01 Jul 2025 13:33:20 GMT  
		Size: 90.0 MB (89951996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f1a503e64117c97e5536892e8c63061df17a168eeb562fc884c0f8e61d8efa`  
		Last Modified: Tue, 01 Jul 2025 13:33:37 GMT  
		Size: 85.4 MB (85355162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9438702337836ae0d219fc9cb4218ad80f5a8409d93dffca47a04e17aba06114`  
		Last Modified: Tue, 01 Jul 2025 02:46:35 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cdb09eda38ef84b2562926d4b1d8d711fe33950d2631cce10b1cb45ae8da0d0`  
		Last Modified: Tue, 01 Jul 2025 02:46:43 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1550-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:03d96922f41e4b4c7d6c82e6082368616a820f64dd710c8ebc209a276fcd4113
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7425589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d28b677f1f55fad5484657fea2b86d6f76e0e8a9efa54bb4796b5a5b430bc876`

```dockerfile
```

-	Layers:
	-	`sha256:d1aa0f448573fc3b874935e9aabfc199bc8db27a674b8ee6307b367c66af2ac0`  
		Last Modified: Tue, 01 Jul 2025 06:41:44 GMT  
		Size: 7.4 MB (7409799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f922676717310a6420c42b816141b08c368e84f93f0d526bccbc075f2a46071`  
		Last Modified: Tue, 01 Jul 2025 06:41:44 GMT  
		Size: 15.8 KB (15790 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.1.1550-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c166f35c310e5f13c30cde8feb932a82ba4353339328628ff37a70fe49f19f02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.9 MB (223910213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c546fab7770b1562de93fdd05e040579f03046d5a65c08504f597995f4a2140`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1749513600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:546a427a0109bbde3a869c6a4ff1ed90ec74768e7fd82dd00441608d83416632`  
		Last Modified: Tue, 10 Jun 2025 22:52:49 GMT  
		Size: 49.6 MB (49621528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6727a70b0f439627ca67f9c6ba9724699951021773f09f699ed385ccc265116`  
		Last Modified: Wed, 11 Jun 2025 08:46:03 GMT  
		Size: 89.1 MB (89091279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3f71271a7578377b8790a99f302805b4b3da5e12bb3c7069fb6636ddd419e2`  
		Last Modified: Wed, 11 Jun 2025 08:49:53 GMT  
		Size: 85.2 MB (85196366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d6e40f00d201f2c3f3376abdde5570b66d6ed5cb73c7224c38049544b269c31`  
		Last Modified: Wed, 11 Jun 2025 08:49:43 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8feccaa0ba0b2392882a48f966f987a5d68feb308ee0a494d80653474bae5c45`  
		Last Modified: Wed, 11 Jun 2025 08:49:43 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1550-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:8e71558c5ef1b4c5118d7242c868d5ede790d2bb89b16eb747aaa5e4979cde58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7432730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c52701f7321a92bb987943b6f2b9a317c919897f004633ed52ba4c5f03fc12`

```dockerfile
```

-	Layers:
	-	`sha256:359f34f47906f0ca1721dddde0864098ba0b48a58fc6e182d8936835a4591691`  
		Last Modified: Wed, 11 Jun 2025 09:42:12 GMT  
		Size: 7.4 MB (7416822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ba25b0ae4b042269a49fa2ef214d59a4eb6c2bcb268c33be489a456556c5058`  
		Last Modified: Wed, 11 Jun 2025 09:42:13 GMT  
		Size: 15.9 KB (15908 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.1.1550-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:de21a1c8f2d10e6860ed2e3d72b1b9d2efeaf1cdebd8c2ed7320bd26546c0fc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.8 MB (233789248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaf0631313b2266be024ecb65b32a3cb44969aa2b38fb781f339788069ef93d7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5c6a246a80c20351fe842a314b6b3f8561a5ceaea736decf36fe380b29e53224`  
		Last Modified: Tue, 01 Jul 2025 01:18:57 GMT  
		Size: 53.1 MB (53097236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:023db990e340f457ab72bf2cfaeeb935b2a5d1eb6d982f2305d773aa3de17226`  
		Last Modified: Tue, 01 Jul 2025 13:21:30 GMT  
		Size: 89.9 MB (89920275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab0b52189bafcadcca120efb4f2c6660a5b0218bf833d78c0b995b306f4dc8f`  
		Last Modified: Tue, 01 Jul 2025 09:20:24 GMT  
		Size: 90.8 MB (90770694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e58cff2cb72256ef4bc5ad9457a6afd1f39a60e2e701b2d45e8bd26c8b2262`  
		Last Modified: Tue, 01 Jul 2025 09:20:13 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641eb09db0289ad382b5bab822d53bb1d1209ff8bea2d06b71843edc1d9b55e7`  
		Last Modified: Tue, 01 Jul 2025 09:20:13 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1550-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:5e672131dc65d54fa040f0d2166cd2aaca1f866d7c4117fd4ecee1dc16d4ae48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7431352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1134b4b59de0f61a3236f5f25b286f48d61528ecc591c4aaac54c82d39092c44`

```dockerfile
```

-	Layers:
	-	`sha256:111591f875cc2bec841252dac1ce7e0443cca0d3687fe8ddf611430862db752f`  
		Last Modified: Tue, 01 Jul 2025 12:38:21 GMT  
		Size: 7.4 MB (7415514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:994d0e3dd9c77d6a0f5e5f61b71925044bf13a41836878ca8a2370c04172a6c5`  
		Last Modified: Tue, 01 Jul 2025 12:38:22 GMT  
		Size: 15.8 KB (15838 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.1.1550-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:d0efb92ea381b5f7bd58e0ebed10d4efd215aa2122ccc82c7c05dfed217896aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 MB (219611590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:892e4b809bcec4629547fea088bfe7daa3fb76aaa292b3ea27a56e10ac553bb8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a19cda6d0aca0ae93b23898ddaa4518ab5077c7011f945c7a7e4a2cacb08ca5f`  
		Last Modified: Tue, 01 Jul 2025 01:23:18 GMT  
		Size: 47.8 MB (47750158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f120b17727d388dbdc6b555b4871b73604f60d8e50666c67171b05dec72894dd`  
		Last Modified: Tue, 01 Jul 2025 13:21:46 GMT  
		Size: 87.6 MB (87622163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3465929612b1cde352b1dad40f146bcb209704e28a8e5a15548e47be7e2ed7f`  
		Last Modified: Tue, 01 Jul 2025 13:33:29 GMT  
		Size: 84.2 MB (84238227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f5cad5cab33ea075270de60c0f480c42b650bb5c9fb772d4bf7b0f6d44815b0`  
		Last Modified: Tue, 01 Jul 2025 03:45:43 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e9eb1478c1d35417f4fbf51951ef6418fe6a55be43698389640c345cfef9c13`  
		Last Modified: Tue, 01 Jul 2025 03:45:45 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1550-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:c876f58b6e5ade7eec1e55753a037ee988a5501e22fca6625f4dfee5e61870ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7413543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4157c1ab7e76531618d841e50c10a8eabc2c713da2e0474a14995b8ae7fe1998`

```dockerfile
```

-	Layers:
	-	`sha256:085d549d8c4469bca11ae21a7bfa7a80e53aab0d8f4228d0db8d92a06909ceef`  
		Last Modified: Tue, 01 Jul 2025 06:42:06 GMT  
		Size: 7.4 MB (7397707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ab398b2a46fd5fa2b10334f865778c90d323dce7e0b0bd57a0771e6749b32ec`  
		Last Modified: Tue, 01 Jul 2025 06:42:07 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.1.1550-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:a84b9c07971384cd49c277aa2670d73adbbc15a9cda3fe4cb0920625a1429be2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.9 MB (220896411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58ded06452574d4fd166a437a7a58162b7005cd78e23639821e8c878d444ac4d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:48de1d8f52c0a2a00375babc11bf69628b8225862d3b6ebbb2205e4ae2f3e96a`  
		Last Modified: Tue, 01 Jul 2025 01:19:00 GMT  
		Size: 49.3 MB (49343660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a364ead8870fff122422a45ac4878c8fdbe3b7a5903e2e3055de1a47697416`  
		Last Modified: Tue, 01 Jul 2025 08:27:05 GMT  
		Size: 85.2 MB (85216885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1debb161ab4bda7842bbf950b430aa7463225a7828d69f3d2e59646e58993018`  
		Last Modified: Tue, 01 Jul 2025 08:31:05 GMT  
		Size: 86.3 MB (86334827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce30651e8fa774d739d658b9ad79832c3c7948a4844f0cdc3d38018bdc18d58a`  
		Last Modified: Tue, 01 Jul 2025 08:30:56 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13f0598e93888d18e3ea8f629895f1e98c4ac7b8dd88ea6881dad94354b5cef`  
		Last Modified: Tue, 01 Jul 2025 08:30:56 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1550-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e91993fa8fa7908907d5c464d626a9536ba3ffd1fdc3e67781dc01649e893f7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7424059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:873a343c539e2d9e09786d35717458d461e128bb66cd89c9c38a1deeff9e9457`

```dockerfile
```

-	Layers:
	-	`sha256:079425768cf94387db2c777538aff0b7eb291804ff1c3b7172c98060340ecfd0`  
		Last Modified: Tue, 01 Jul 2025 09:41:44 GMT  
		Size: 7.4 MB (7408269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76fc72856a30157ae251a6443ec6756813124eb92a1eb4826204b8c344ec9cc0`  
		Last Modified: Tue, 01 Jul 2025 09:41:44 GMT  
		Size: 15.8 KB (15790 bytes)  
		MIME: application/vnd.in-toto+json
