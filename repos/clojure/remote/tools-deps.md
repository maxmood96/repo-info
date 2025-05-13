## `clojure:tools-deps`

```console
$ docker pull clojure@sha256:b6f1c16d4bf277fd32e739ddcd0fabe64d25d32a4c281034cee5e62b5b5d822c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	linux; s390x

### `clojure:tools-deps` - linux; amd64

```console
$ docker pull clojure@sha256:75420108438e7cb3be5fc496484c0502d53dd96106be5faedb93fab95f1e8644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.1 MB (287118197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:543381e35e5c8d3566412b18da2b41eb6c8d53daf90146bb8414d3e06e34f548`
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
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 48.5 MB (48491199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa70317dd6396cacc011b4373d753fa50d77879e2ef781bc76f1b9269980f58c`  
		Last Modified: Mon, 05 May 2025 17:08:27 GMT  
		Size: 157.6 MB (157634443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637ef880bd7d16b7d404cad1047e400e9f5473b01069b957e09c886b9a68cf05`  
		Last Modified: Mon, 05 May 2025 17:08:27 GMT  
		Size: 81.0 MB (80991515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf7880523c428fce7be2bc3c7228d0c06d82690a8cc243aa0c527ebda3d1ee0`  
		Last Modified: Mon, 05 May 2025 17:08:25 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7100d440174f32ded5d830e5f8d7d4749d54363da13dc44f96e6e6944ae5874`  
		Last Modified: Mon, 05 May 2025 17:08:25 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:ff05b3cb504887b98236625e3f9daa8b38eb41f6d4f3433859779b6210e1ff2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7195399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46ccef0182f0e17ac6227771b2c0a9db8185ac6141f171ce7eccf34ee2f3ca53`

```dockerfile
```

-	Layers:
	-	`sha256:34e869c943c581f19ca555eff9d5ab47afac50697ca0e71653674662eae0c322`  
		Last Modified: Mon, 05 May 2025 17:08:25 GMT  
		Size: 7.2 MB (7177578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d8c57f97c0e58cdcbf32ff9c6e2e270008a3aee224fa4a0ef24745b29a5fad3`  
		Last Modified: Mon, 05 May 2025 17:08:24 GMT  
		Size: 17.8 KB (17821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c12a38d854a29a2a6aeed89586bf073f1180b1f78515874f76514fc9f2214a37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.1 MB (285101207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c513b4b942d08e7cdabaac74808c0364e6fe029e4f3a9fb00b9683d31080cc2`
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
		Last Modified: Mon, 28 Apr 2025 21:20:23 GMT  
		Size: 48.3 MB (48327644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d189b2fb377f95831046c31bd397aceb2f08b6580d5bd75e7b63e07168cab2cd`  
		Last Modified: Wed, 30 Apr 2025 00:57:50 GMT  
		Size: 155.9 MB (155928805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d102db49e0d3933a64ee46ad10e6477515a2581dae4db9f082cbe937f0a54e`  
		Last Modified: Wed, 30 Apr 2025 01:44:59 GMT  
		Size: 80.8 MB (80843718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809fb8e3d4b23c61cac7fdc8f19558b6f0b9190a8e8b2dc7c8baa21ae6391f2e`  
		Last Modified: Wed, 30 Apr 2025 01:44:56 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c452a197b72d4fa6c36be84308f7b8208ffe83deccc2cbcc1f3e9fedb73aeb6`  
		Last Modified: Wed, 30 Apr 2025 01:44:56 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:c6675d4fae97a18d8d939d677d7734c33e3de4b31eaaaa91968886c914da6b90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7201423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89fe042bec176e547e61ef06d3b8247628c878199cea6ae48a1defecd21c79d5`

```dockerfile
```

-	Layers:
	-	`sha256:d30fbd54e7fd45ca41b73c5d80d9b9c4cfad3508607d592b4dd402d18fb95428`  
		Last Modified: Tue, 06 May 2025 00:43:48 GMT  
		Size: 7.2 MB (7183413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b3aec6e52cfedcedff99bbea6aa522a3d5fd879fe538f3e6dd1ea4cc6bc6d22`  
		Last Modified: Tue, 06 May 2025 00:43:48 GMT  
		Size: 18.0 KB (18010 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps` - linux; ppc64le

```console
$ docker pull clojure@sha256:a97a4c71cbcbc767fb7eb4aa1d06bd27ad0dee1192001d93317ae525f1290c6b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272605631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9a8005d5c97f2d364e3dc62026bdfbb5f6c9e2c347a62ac84e2b5ef6c63d300`
-	Default Command: `["sh","-c","sleep 1 && exec clj"]`

```dockerfile
# Wed, 08 May 2019 09:03:26 GMT
ADD file:844cea0aa071f0f6b2640d4c452590a8777485fa27a0aad789553110eaeb7081 in / 
# Wed, 08 May 2019 09:03:33 GMT
CMD ["bash"]
# Wed, 08 May 2019 12:06:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 12:07:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 08 May 2019 12:09:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 12:29:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 12:48:27 GMT
ENV LANG=C.UTF-8
# Wed, 08 May 2019 12:48:35 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 08 May 2019 12:48:42 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 08 May 2019 12:48:44 GMT
ENV JAVA_HOME=/docker-java-home
# Wed, 08 May 2019 12:48:47 GMT
ENV JAVA_VERSION=8u212
# Wed, 08 May 2019 12:48:49 GMT
ENV JAVA_DEBIAN_VERSION=8u212-b01-1~deb9u1
# Wed, 08 May 2019 12:54:27 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y --no-install-recommends 		openjdk-8-jdk="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 02 Jul 2019 14:36:37 GMT
LABEL maintainer=Kirill Chernyshov <delaguardo@gmail.com>
# Tue, 02 Jul 2019 14:36:40 GMT
ENV CLOJURE_VERSION=1.10.0.442
# Tue, 02 Jul 2019 14:36:46 GMT
WORKDIR /tmp
# Tue, 02 Jul 2019 14:37:15 GMT
RUN apt-get update && apt-get install -y rlwrap
# Tue, 02 Jul 2019 14:37:51 GMT
RUN wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh     && chmod +x linux-install-$CLOJURE_VERSION.sh     && ./linux-install-$CLOJURE_VERSION.sh
# Tue, 02 Jul 2019 14:38:15 GMT
RUN clojure -e "(clojure-version)"
# Tue, 02 Jul 2019 14:38:19 GMT
CMD ["sh" "-c" "sleep 1 && exec clj"]
```

-	Layers:
	-	`sha256:c6c4df30bc4ffa8fb97a3dda6f8758fb0ddeb8929d159369cf5974dd3f2ac117`  
		Last Modified: Wed, 08 May 2019 09:21:32 GMT  
		Size: 45.6 MB (45603184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8b6d64c78121ab5074c55b90272e1a13e72e3b7854d6a6c7e638eff77307ba`  
		Last Modified: Wed, 08 May 2019 12:24:57 GMT  
		Size: 10.0 MB (9991084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:663d68dc2e1243453bf4b04afcb5394452ca5371b05a1c96f41a0df4189631e8`  
		Last Modified: Wed, 08 May 2019 12:24:54 GMT  
		Size: 4.3 MB (4296597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb9e53310a32438c1469c44f0a134314d8c4091b5ffa8f58fef5357ff3633415`  
		Last Modified: Wed, 08 May 2019 12:25:56 GMT  
		Size: 50.1 MB (50071573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d238037ed96ca39723b2ee324978c74743556692baf6e9eb42bd21fe63186281`  
		Last Modified: Wed, 08 May 2019 13:10:34 GMT  
		Size: 886.4 KB (886422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6acf537adb79f65e1ac82c6970a4b627a94053cf6b9f665c2f7983b4e99e803`  
		Last Modified: Wed, 08 May 2019 13:17:48 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71ce554fdde0e1f8c296846b4ccda3c305752e078d12bcdba6740ea209df6a49`  
		Last Modified: Wed, 08 May 2019 13:17:48 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba7c9b555677504d9d96cbd389b1537f645ebcd4f3c671cde8d4c14bd3c62fd`  
		Last Modified: Wed, 08 May 2019 13:19:01 GMT  
		Size: 125.1 MB (125136529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57cb6ef01bc0667a67edd90e6b28be4dbb68b12f6eaf93cbbc5b581cd41d72ea`  
		Last Modified: Tue, 02 Jul 2019 14:45:49 GMT  
		Size: 12.7 MB (12748204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:544625e5a46cbc6576dbbbd8ad794b981ef72a45dd516624aaa26cddde75ff01`  
		Last Modified: Tue, 02 Jul 2019 14:45:49 GMT  
		Size: 19.8 MB (19768871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e7cb91047bea27016b85bcdba35f685fd3417b02edb04afbb9b1ac575790a0e`  
		Last Modified: Tue, 02 Jul 2019 14:45:47 GMT  
		Size: 4.1 MB (4102787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:tools-deps` - linux; s390x

```console
$ docker pull clojure@sha256:75a34a0c0abd2652abb9f15b88e1931d14efa40ece815a4a62d0fc9227eee5d6
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.3 MB (271322198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf9c9869091c1012eca6dd9a85f6f9d236dbcdd98c7113bb80464beb86608f5e`
-	Default Command: `["sh","-c","sleep 1 && exec clj"]`

```dockerfile
# Wed, 08 May 2019 11:46:30 GMT
ADD file:35b243252442c1fc6a9e4f7bea498f5b7302c530eb804ed6a79c5b84a68a96fd in / 
# Wed, 08 May 2019 11:46:31 GMT
CMD ["bash"]
# Wed, 08 May 2019 13:48:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 13:48:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 08 May 2019 13:50:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 14:35:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 14:47:53 GMT
ENV LANG=C.UTF-8
# Wed, 08 May 2019 14:47:57 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 08 May 2019 14:48:01 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 08 May 2019 14:48:02 GMT
ENV JAVA_HOME=/docker-java-home
# Wed, 08 May 2019 14:48:03 GMT
ENV JAVA_VERSION=8u212
# Wed, 08 May 2019 14:48:04 GMT
ENV JAVA_DEBIAN_VERSION=8u212-b01-1~deb9u1
# Wed, 08 May 2019 14:50:36 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y --no-install-recommends 		openjdk-8-jdk="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Thu, 09 May 2019 03:29:00 GMT
LABEL maintainer=Kirill Chernyshov <delaguardo@gmail.com>
# Thu, 09 May 2019 03:29:00 GMT
ENV CLOJURE_VERSION=1.10.0.442
# Thu, 09 May 2019 03:29:01 GMT
WORKDIR /tmp
# Thu, 09 May 2019 03:29:20 GMT
RUN apt-get update && apt-get install -y rlwrap
# Thu, 09 May 2019 03:29:27 GMT
RUN wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh     && chmod +x linux-install-$CLOJURE_VERSION.sh     && ./linux-install-$CLOJURE_VERSION.sh
# Thu, 09 May 2019 03:31:10 GMT
RUN clojure -e "(clojure-version)"
# Thu, 09 May 2019 03:31:12 GMT
CMD ["sh" "-c" "sleep 1 && exec clj"]
```

-	Layers:
	-	`sha256:3602dd773e45048fcb10569c368bf7ddac54267760f371efbe1bb65ba8d67361`  
		Last Modified: Wed, 08 May 2019 11:52:15 GMT  
		Size: 45.2 MB (45197648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:412a17b553a57c91ed490be0279a1aafa108b9a60b10f8c482ed85ca94de3a3c`  
		Last Modified: Wed, 08 May 2019 14:00:34 GMT  
		Size: 10.3 MB (10314565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5007dca2cc2afa05648742b75324a09e45eae504d384750ed7c6de3e5e5d65d2`  
		Last Modified: Wed, 08 May 2019 14:00:30 GMT  
		Size: 4.4 MB (4372280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:612e650c4b45ea187d6b0fe7fe4970d9e11c683da76c8eaf7616753930f2c3ec`  
		Last Modified: Wed, 08 May 2019 14:01:09 GMT  
		Size: 50.5 MB (50489726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf3d4edfd5ed38100e9ec60c73a23fc10666fc5d20cc6a47fc37e92beded5bfc`  
		Last Modified: Wed, 08 May 2019 14:58:42 GMT  
		Size: 903.9 KB (903862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dce2c7ff96eda7fdeada798d3a8f7ea30b4c253a054620b9fd97f3595c2da39`  
		Last Modified: Wed, 08 May 2019 15:03:03 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fecd9e4a7568c8232cac170b5ae083c06c3b36fd96cf7afafb082c5e91a2c078`  
		Last Modified: Wed, 08 May 2019 15:03:04 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e54837587b8fa7b02484a021fbd8f809e9d8432d52825551839a60e4e3f9ebd`  
		Last Modified: Wed, 08 May 2019 15:03:44 GMT  
		Size: 124.1 MB (124111932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e7383fe5474dfbd8d57cdb07092ab9c79147baafae1611fd2bdcf27a6eebcf`  
		Last Modified: Thu, 09 May 2019 03:39:00 GMT  
		Size: 12.1 MB (12060296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b7c0a86ede97928fa88a370d379fdb0b18063b7948af3de5ba57caca6b27ac4`  
		Last Modified: Thu, 09 May 2019 03:39:00 GMT  
		Size: 19.8 MB (19768751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94f60d43a05a93ad3974dafd9a09c2ae3486e05fc08b6cba4202c3c875b0ad4e`  
		Last Modified: Thu, 09 May 2019 03:38:56 GMT  
		Size: 4.1 MB (4102758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
