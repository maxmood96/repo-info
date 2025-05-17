## `clojure:temurin-24-tools-deps-1.12.0.1530-bookworm`

```console
$ docker pull clojure@sha256:ec52ccbca2d23d13f6f2d64b5234c3536dd222559f619c274c4dc29a2174393e
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

### `clojure:temurin-24-tools-deps-1.12.0.1530-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:67acdf82a5d775b03cfdd718acd156c8da7802061aab1f09f7bbd0315b83c863
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 MB (219435570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85b4438a4ab84c45027f9e69a2ec1a6e78cde01ba5ad5e2e5c2d72599d103e42`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:cf05a52c02353f0b2b6f9be0549ac916c3fb1dc8d4bacd405eac7f28562ec9f2`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 48.5 MB (48491199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb316c44e85ab2137ae62886f269e7f0e2add5d272864871ec38363f08d148d6`  
		Last Modified: Fri, 09 May 2025 13:06:45 GMT  
		Size: 90.0 MB (89951992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6965be0efc60af1211af360319a909bd15349ab68f03422c0870282b3df0974`  
		Last Modified: Fri, 09 May 2025 13:06:37 GMT  
		Size: 81.0 MB (80991344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e47679ef67ef142c1b84318542429e072f9d93bda0bd74323999789bf1ff9536`  
		Last Modified: Fri, 09 May 2025 13:06:30 GMT  
		Size: 609.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8c6be7ffd5949420596988861aa1a0c47f736c781243be377e44ae5cccc39a`  
		Last Modified: Fri, 09 May 2025 13:06:31 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.0.1530-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:5b74a282ce289d007016912244761b2848aa3410b24b6297cdf2967432bb642f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7140304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88b648b1328dd6ce1d1044899a1457e50cbffeeed1a1f67024c699b4e89d4258`

```dockerfile
```

-	Layers:
	-	`sha256:702f92fb7bc51d86b27dce4358a327d7d98e489fdc2baaa116f2014168f8fe16`  
		Last Modified: Mon, 05 May 2025 17:07:55 GMT  
		Size: 7.1 MB (7123806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:017d374bb26d1ed9123574206d4ae346b2a2695ddb71bf64fb25224011233b84`  
		Last Modified: Mon, 05 May 2025 17:07:55 GMT  
		Size: 16.5 KB (16498 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.0.1530-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:515d21ba904180a8bc0bbe856d6ca9d1715fb0ce4420103447df65b538fa0a27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.3 MB (218263772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce830c1a4927567ff87f0c73a4e1c3b6ef0643b37447c90fedeb348ba52a0892`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:de07ba6f486e0ce29760ab32d4381edabbc660a04c493e95eb9a8056925d8955`  
		Last Modified: Thu, 08 May 2025 17:04:44 GMT  
		Size: 48.3 MB (48327644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289d29a9fc32a83e7866e7172e5148e804d7fa6b5e264bedd1edcbb3907d41e8`  
		Last Modified: Sat, 17 May 2025 17:48:01 GMT  
		Size: 89.1 MB (89091234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceec8f5e8b270bccbb1e7666f3c2abf66341fdddb2d080897610d749047b6afa`  
		Last Modified: Sat, 17 May 2025 17:48:01 GMT  
		Size: 80.8 MB (80843855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f1f42350d9b5f1ccbbd8b67ad5421bf6b535226ea54a3cac188a895fd67119`  
		Last Modified: Sat, 17 May 2025 17:47:45 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d097471bb254acff10d2de2adc6a2b59e987200d20b70444a753ff93a5c256c`  
		Last Modified: Sat, 17 May 2025 17:47:44 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.0.1530-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:aa4ff138459002a4a5d040cadc744e1451b7bf6271dc71f481bab80aec0b1710
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7146230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeaabea75c0c2df0ef9262ba92400deadf674aefb462e96e75107316ad2cdc8f`

```dockerfile
```

-	Layers:
	-	`sha256:ac7aeb91f24c53cc8099d93dadfbef6b0ab331028ef10a6ea86e0f787aa57c3b`  
		Last Modified: Tue, 06 May 2025 00:49:09 GMT  
		Size: 7.1 MB (7129590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fda7866b0591fe2c6a7a95ba60d2394717b2b88f078db9b5d0a98ae1c118dfd6`  
		Last Modified: Tue, 06 May 2025 00:49:08 GMT  
		Size: 16.6 KB (16640 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.0.1530-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:5efce8b054a9bd37ca1c43f26b6cb56c041ae414159c43b1d4f0dc7d28738338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.1 MB (229053950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a994afe0bec507d7a1b2087012c27b9bf586ba2e29045d540484c7a7f2257913`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:33862e890d6c23fba01df0303b503e727dad5c72574fdf8af76d76dc3140d561`  
		Last Modified: Thu, 08 May 2025 17:13:17 GMT  
		Size: 52.3 MB (52332129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667e2c75575ea3101085eedee6465ccbd4328518899a2687f5acfacb51334a63`  
		Last Modified: Tue, 13 May 2025 19:30:24 GMT  
		Size: 89.9 MB (89920243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dd7e2b65b98e4943fc1c0d97215ab7173f28e50f8d942fef383bbcc6ffb8bdf`  
		Last Modified: Tue, 13 May 2025 19:38:37 GMT  
		Size: 86.8 MB (86800534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a66566290fc530774f47a548dcc1c1126c663a0dc682336dd072c7949537d5d`  
		Last Modified: Tue, 13 May 2025 19:38:35 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f697213d09092441387351a3c940aab7175dc877c8100504aff5f12561379d7b`  
		Last Modified: Tue, 13 May 2025 19:38:35 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.0.1530-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:23e33ba86718290351d3f8f8c1d7060add97707525f2e3765d98b7d1cf04cb72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7146716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:293a30e2103314794603631b3d9d10d176eaaf2403df866b8306a673f69261a0`

```dockerfile
```

-	Layers:
	-	`sha256:ff84827594c5b20dacad49505db4a319de863a344a4de7d744c0db4ba7377a87`  
		Last Modified: Tue, 13 May 2025 19:38:35 GMT  
		Size: 7.1 MB (7130158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f934688c4cf4165e64003562596009a2368fb313a1428cb60c8a7a2890f7735`  
		Last Modified: Tue, 13 May 2025 19:38:34 GMT  
		Size: 16.6 KB (16558 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.0.1530-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:3f7b7799bf8d48f914ba70e5624f24808309268426e93ada16696b74a380f9a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.2 MB (212165774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb0df5c51b6c74f5bceeb043bd4a64fd069b2eecdb2c1234b52d01c8028fd8ff`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a5e7ec27bb28a531688c62bada8c4b448d8e280327ecabb8be798bc43be30c38`  
		Last Modified: Thu, 08 May 2025 17:04:50 GMT  
		Size: 47.2 MB (47151332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e5543a7e7f181a87f4b54a4806466f043c954887fbd8349c3543edf7cd2f7ab`  
		Last Modified: Tue, 13 May 2025 18:34:02 GMT  
		Size: 85.2 MB (85216805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f555eaaa94da70a530cfc9cdcb30cc98360d027abc8ce8435cf8a4125eb9b3ae`  
		Last Modified: Tue, 13 May 2025 18:41:00 GMT  
		Size: 79.8 MB (79796601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a049427ae0159fe5ede1c473ffcec19f8dc4022fe2f2ad3a9d9deba4fcaed08`  
		Last Modified: Tue, 13 May 2025 18:40:58 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fbd4d9be6b0a383235aa23daaaba58043ff4c1da8120910ba9b4b68b799e875`  
		Last Modified: Tue, 13 May 2025 18:40:58 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.0.1530-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:ed52a7ceea143c8cd040d823122cbbddd67b33a23e8ead4e036baea64ea11e5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7137063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:255100d1f8c2a49ba90b8e8822bf73106d07c2d6d0a88d152c026c5d7cb420d8`

```dockerfile
```

-	Layers:
	-	`sha256:3ab6a82a4bf78d2c02e2012686ba15372fa6ff25ba64f9e34d892ac77b8f5e3c`  
		Last Modified: Tue, 13 May 2025 18:40:59 GMT  
		Size: 7.1 MB (7120565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad83f71a6471853a6ab1edb4468cd8f1086482e1a4d44b9ca4b982abd5039f57`  
		Last Modified: Tue, 13 May 2025 18:40:58 GMT  
		Size: 16.5 KB (16498 bytes)  
		MIME: application/vnd.in-toto+json
