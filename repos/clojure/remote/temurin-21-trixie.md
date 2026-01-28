## `clojure:temurin-21-trixie`

```console
$ docker pull clojure@sha256:18b6a1db2c84c0fd67c4c2eacd5fa9ef1a4d048174fa72175fc8f4976dec0d16
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

### `clojure:temurin-21-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:713cf728a50ba56836979fb17cab3e87520bcf4e62123634060efafef14d9c57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.6 MB (295626352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2210f1843711abb615b746a1da7e81415c930f49507cd559ac6dce7f527e9839`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Wed, 28 Jan 2026 18:05:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:05:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:05:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:05:59 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:05:59 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:06:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:06:16 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:06:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:06:16 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:06:16 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2ca1bfae7ba8b9e2a56c1c19a2d14036cae96bf868ca154ca88bc078eaf7c376`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 49.3 MB (49285621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e69184b89c4ee025fce25f8907cfe9fff2e265521a47c42441d85789a7cc30a`  
		Last Modified: Wed, 28 Jan 2026 18:06:41 GMT  
		Size: 157.8 MB (157825978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de4b6a09cf9272b04102dafa6247ea08eb18b803191ea1667c30d4474b776f84`  
		Last Modified: Wed, 28 Jan 2026 18:06:40 GMT  
		Size: 88.5 MB (88513708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:468af183ecd3f75f76cd9902395a1539884a6468a50fa0b6e4002f8694ec3b93`  
		Last Modified: Wed, 28 Jan 2026 18:06:36 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4894897a8d570cda2cedc062c5ad3269ad38c5923ccba6ff27603a2912c70c01`  
		Last Modified: Wed, 28 Jan 2026 18:06:36 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:57110805188989f6d073dc523c8ca5d125196c999bf584f05f9b67ade7b10125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7486684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a957e1266ee75b9b2619b7fd4d77c982787ddd768110ba15d6ee6ebab931faa8`

```dockerfile
```

-	Layers:
	-	`sha256:a7764797889b2cb674c501aae7ac32d424afded5c5d3be485c202eae52505f69`  
		Last Modified: Wed, 28 Jan 2026 18:06:36 GMT  
		Size: 7.5 MB (7470930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d81e617582d4e5d23be5cecd02c4730655e6c8ff95307e770a954f4b719fe82`  
		Last Modified: Wed, 28 Jan 2026 18:06:36 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1de63a431ed21eed2249026b5b68ab20a0034577157a4280a257a934940a7b19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.4 MB (294449255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33c9cb9d7c02943a530658616bd4e89a11de476dd94bab2f589b0ef509f87483`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Wed, 28 Jan 2026 18:05:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:05:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:05:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:05:29 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:05:29 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:05:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:05:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:05:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:05:49 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:05:49 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5582010cab7f00a8f96e076b02666116eaa7e4af9a74eb44f2946a593b50294f`  
		Last Modified: Tue, 13 Jan 2026 00:42:42 GMT  
		Size: 49.6 MB (49648083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc8d849675c709d925d4917b93e2fcb412dce52186cb096382181f40f8d6e1ba`  
		Last Modified: Wed, 28 Jan 2026 18:06:14 GMT  
		Size: 156.1 MB (156107578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46ae07bb6b32f2311f1794c1808c04635f9c926cadc1bbd258a2b1ec617f7db`  
		Last Modified: Wed, 28 Jan 2026 18:06:12 GMT  
		Size: 88.7 MB (88692554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91f3af0b1655cd3a2c5c9f04f1dda71a8528cdf15ab0e543a6f7bea74e37495`  
		Last Modified: Wed, 28 Jan 2026 18:06:09 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76934dcb5fcf216672710dae3b5865d5045e20918adb64426cf96f9f204d6ef1`  
		Last Modified: Wed, 28 Jan 2026 18:06:09 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:5ce20291252e78e6c7ef3360fde8ba8a74ec29848ce5cdcaa098c6016166005d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7493832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:189a54fb1cf8573ee2fe4c067f7c3c0c2187983a006c30563562e7d32c9b0139`

```dockerfile
```

-	Layers:
	-	`sha256:8e03c9e395d559f44fd764eed31c3a3362af2493689b60d54bb27e8e55298ae9`  
		Last Modified: Wed, 28 Jan 2026 18:06:09 GMT  
		Size: 7.5 MB (7477960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ca13121a92f503554a6165e927e6f67b684f50ce357ead6f19857a9494edcdb`  
		Last Modified: Wed, 28 Jan 2026 18:06:09 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:9511ee590f3a2493b80463724217dfa5588357959f5ca99a51c93ab94e24959e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.2 MB (305203821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e9f779f081b356f7e2d3e3ef7ff2cfca6e2683132d8fdb2626ffcc244ed0a28`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Wed, 28 Jan 2026 18:29:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:29:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:29:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:29:53 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:29:53 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:31:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:31:08 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:31:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:31:08 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:31:08 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6ff412c1efdf82a2030de7bb593b97f09e02e2b337f615eb1c3faedeef765d44`  
		Last Modified: Tue, 13 Jan 2026 08:45:48 GMT  
		Size: 53.1 MB (53106962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea87e0e784dfe85d8229ea938fdb15a9cacdb83d0d027e8baaa0ecde041410f`  
		Last Modified: Wed, 28 Jan 2026 18:31:54 GMT  
		Size: 157.9 MB (157942993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d398edbc6fc721fa46395321fe65ef2a86da27b1128ac7edc6da0f0a5ef04e3d`  
		Last Modified: Wed, 28 Jan 2026 18:31:52 GMT  
		Size: 94.2 MB (94152822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8585460290d270fd54ba69f7bd8c6c45c7974a6d812121d082365bd9dfc471aa`  
		Last Modified: Wed, 28 Jan 2026 18:31:48 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b18b5692e13a66de89c7f948d3e20ae6429dc06409366043ff7095b393808e`  
		Last Modified: Wed, 28 Jan 2026 18:31:48 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:94188ba1324cdbe9020b27a28c5d96d87ad7865fa67637dbe818a1854e46e0de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7491153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b63bc1c8585ad4170fd8a50c4aca2d4100560f1724d3dd8dea73afc31a321bb`

```dockerfile
```

-	Layers:
	-	`sha256:8552a76710d249d59250b667e966dff5752ff3474b2a4ea73df39728f52c92fe`  
		Last Modified: Wed, 28 Jan 2026 18:31:49 GMT  
		Size: 7.5 MB (7475351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e15dfc3105b4243e751614a2b216618d1ed51f53909d03a9780cdb2df5d5ad38`  
		Last Modified: Wed, 28 Jan 2026 18:31:48 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:b20302266a24bd1d322e1163913cbb61394f97fb29d74821f050b19847940705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.4 MB (289390162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aabe4a8ae3196f83ae5776053eb20bad676ee5a9dbfbd932e2cd95e35af1cb4d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Thu, 22 Jan 2026 03:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Jan 2026 03:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Jan 2026 03:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jan 2026 03:51:04 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 22 Jan 2026 03:51:04 GMT
WORKDIR /tmp
# Thu, 22 Jan 2026 04:13:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 22 Jan 2026 04:13:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 22 Jan 2026 04:13:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 22 Jan 2026 04:13:45 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 22 Jan 2026 04:13:45 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:559020494fc8527e77b291bee49cdac1db6bca66f8926cda195e0e4ebe7d2d3d`  
		Last Modified: Tue, 13 Jan 2026 01:06:14 GMT  
		Size: 47.8 MB (47770843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ed654d72f1583479eae71ff4bca91d394293fa06b9e1bd650a8ac986e87dd2`  
		Last Modified: Thu, 22 Jan 2026 03:57:33 GMT  
		Size: 157.2 MB (157194267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db0b8789669bfb079125ce0cfd40cb5fd2db09e819a9b432424db92baa4eb284`  
		Last Modified: Thu, 22 Jan 2026 04:18:18 GMT  
		Size: 84.4 MB (84424010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1644670c2a95fd4dee2151d45b57d1d201fedc283eb9ce270cf308b0af0992d1`  
		Last Modified: Thu, 22 Jan 2026 04:18:05 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830671b3afc0e3187c461545c74ac6d032188299215aae9b704b84a1819a1c6a`  
		Last Modified: Thu, 22 Jan 2026 04:18:05 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:0be28f07b981b0fddc31beffdd5faedf33452648ce75727239ebcb58f5d10003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7474645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80c971f987634a5d2c188a1e5d5a1cdafa5088bedd4de92b03c63465275312fc`

```dockerfile
```

-	Layers:
	-	`sha256:4c6f80093c8b750f2c98f6f90799b5b93a0913529fb8aee37b2b92de100c78c0`  
		Last Modified: Thu, 22 Jan 2026 04:18:07 GMT  
		Size: 7.5 MB (7458843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64523b217105fcac2580e39a97f02e62236330611f6935e5ed6930096f793c96`  
		Last Modified: Thu, 22 Jan 2026 04:18:04 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:409086e727873c47bf0b7284042261f80e90305882ed5939adf1f08edc39fffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.6 MB (285551240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20965de8911d8e47239cffced65cc4ce76d2b80c4dcdae81d4d4b200b49aa6f7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Thu, 15 Jan 2026 23:18:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 23:18:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 15 Jan 2026 23:18:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:18:53 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 15 Jan 2026 23:18:53 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:14:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:14:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:14:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:14:06 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:14:06 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9de0288d81a9602539c9f3015fc521191e25eebfe6442c22cb974ea3a486f3a8`  
		Last Modified: Tue, 13 Jan 2026 00:41:46 GMT  
		Size: 49.3 MB (49348704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe546673f26304e6e3a7565a4a244298cac2a8e593d48a999166ccef6a08f73`  
		Last Modified: Thu, 15 Jan 2026 23:19:35 GMT  
		Size: 147.1 MB (147069857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c404aebe88c70590d87ee0959a36d7a62042b3cb7be702b87d93896bc7193d`  
		Last Modified: Wed, 28 Jan 2026 18:14:35 GMT  
		Size: 89.1 MB (89131638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb92d99a61b2dcb05d93c0a2c937f8913ca560d07f8337fd0685d3e82317103`  
		Last Modified: Wed, 28 Jan 2026 18:14:33 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4232e72072b2da658145d53f878fe2f242d5fa0c08987e18a32c845cb4e14cc`  
		Last Modified: Wed, 28 Jan 2026 18:14:33 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:2221fbe36ca0fbf0493cb883691de30b486fc3c9d033b87030906c09314fb0b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7482605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf1d51a4cb5ff6475c61a682d9cd15a7eb583c281b435d37ac5175e2b2782f24`

```dockerfile
```

-	Layers:
	-	`sha256:cdeb691149acbe8408414c63c4890b821b1566396a31e7a4ffb7b46ef7456545`  
		Last Modified: Wed, 28 Jan 2026 18:14:33 GMT  
		Size: 7.5 MB (7466852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1aed95151088e590a30786680c014e8e7739566edad7c9294939ad0e44ae3afc`  
		Last Modified: Wed, 28 Jan 2026 18:14:33 GMT  
		Size: 15.8 KB (15753 bytes)  
		MIME: application/vnd.in-toto+json
