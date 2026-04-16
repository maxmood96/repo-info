## `clojure:temurin-25-trixie-slim`

```console
$ docker pull clojure@sha256:042d4124681c0a66dde735375c6f570ccdb92c3f99b3cf014d9ccdf327846a66
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

### `clojure:temurin-25-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:21c6fde92bd34f79022e9ed9b0641a410d9221ad1fd1c7ae8bce2946f50938f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.0 MB (197009552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49edcc0433f09c812db89286fbbe35f31933207dabded663a28fc12f61afaaba`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Wed, 15 Apr 2026 22:06:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:06:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:06:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:06:59 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:06:59 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:07:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:07:15 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:07:15 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:07:15 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:07:15 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d873671160757ddbc1db486d8adf05d1d860d261f694b15d6cb7438f9ac52ae0`  
		Last Modified: Wed, 15 Apr 2026 22:07:36 GMT  
		Size: 92.3 MB (92256319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43302f7006cfb5d1286a5f88ef527b15db16ce556b34c187737ca4cdfc31faf9`  
		Last Modified: Wed, 15 Apr 2026 22:07:36 GMT  
		Size: 75.0 MB (74976549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9cc001a1dab17ffd46c5845565009c5826f83cad96f5d5b5842ebd903ff9b7`  
		Last Modified: Wed, 15 Apr 2026 22:07:33 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08d71867508e9ab94b8cfcf9560a93a1314a69f947560391a8485236d80f0edf`  
		Last Modified: Wed, 15 Apr 2026 22:07:33 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4a97b783c7b6fdf9aea6d46ba150e16597c702cdcf9f02a3f3689bd2cc66779c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5243717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50ffeac62167902dae0db578eec4ffc6f6ebce9f516f2e1934e7017aad40adb4`

```dockerfile
```

-	Layers:
	-	`sha256:93afd93241d7c5c8699425a0dc9afe45e06c388b09a70ac41911f6c2b4d9d953`  
		Last Modified: Wed, 15 Apr 2026 22:07:33 GMT  
		Size: 5.2 MB (5227224 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e17c8fba3615b9ed0b0bca63c24fb3262945a8f71f4d05ddd7eb22f9a69a3aa`  
		Last Modified: Wed, 15 Apr 2026 22:07:32 GMT  
		Size: 16.5 KB (16493 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f1b00da4d9b76fd74752b287b573b15a871a552c6344ee30ccf5cbcd59cdba69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.6 MB (196577071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b3b5b7566924c7a3abf5d0135c70962c5332c3997db16f5bb21c61c703b6e52`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Wed, 15 Apr 2026 22:18:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:18:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:18:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:18:49 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:18:49 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:19:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:19:09 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:19:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:19:09 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:19:09 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b308aa5eb97f4ccaba0ab4f7a7513687499487cfbf157940a48fc2a646d202fc`  
		Last Modified: Wed, 15 Apr 2026 22:19:32 GMT  
		Size: 91.3 MB (91288274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ff6f7f0aa3c441437d909eb78c6badb678635de99427a063374726f2fff2f5`  
		Last Modified: Wed, 15 Apr 2026 22:19:31 GMT  
		Size: 75.1 MB (75149207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ce6f88380ba7258ab90ccf5ff6144eeb9499f9b5ba83449a7f3b22eda2cccc`  
		Last Modified: Wed, 15 Apr 2026 22:19:28 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68485a94a913cd9864a5ba7c60760ca5e9e93829e63d8566e8689864ae8af29a`  
		Last Modified: Wed, 15 Apr 2026 22:19:28 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4fb61d0a6c11b4aec889c59be105e674d4f7b2150c910e3b30c63caa7f17aa01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5249649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6d9915b547da8986b18e99c73353c92f24d9756354c5389a8f059701b852e9b`

```dockerfile
```

-	Layers:
	-	`sha256:38d4709fe844c04898dc7639c2b1e35330c92c273300518d0090e895eff45bb0`  
		Last Modified: Wed, 15 Apr 2026 22:19:28 GMT  
		Size: 5.2 MB (5233014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09ed77fbda56b6c3eac275ac123adee83b110f27ad9e5fe04ff2416bf449d74b`  
		Last Modified: Wed, 15 Apr 2026 22:19:28 GMT  
		Size: 16.6 KB (16635 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:6203e338743ebadb1fbe468c168159cfbb242fd31fd3b93bf3ec144d34848547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.7 MB (202656223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5abe8ad945d9bb400b4a86937df90baafbc6712e82a88aef90bda0948a72bb1f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 14:57:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 14:57:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 14:57:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 14:57:19 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 14:57:19 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 15:06:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 15:06:09 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 15:06:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 15:06:09 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 15:06:09 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6e3428d4efac15fe7728b465c9c3bc5d71a07ad502becbd70250a2c560e32b53`  
		Last Modified: Tue, 07 Apr 2026 00:12:50 GMT  
		Size: 33.6 MB (33593016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:674dad765dcc78e0a3938a692ea5b290c37a0c10042e2a743ec14ddef8e6b775`  
		Last Modified: Tue, 07 Apr 2026 14:58:42 GMT  
		Size: 91.6 MB (91633035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3117a1906e5350225d23f3930acda18fcd4628b02646bc3720b97a0c27d4ff`  
		Last Modified: Tue, 07 Apr 2026 15:06:47 GMT  
		Size: 77.4 MB (77429128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b35bc6399945036da62d8f683b7adf2588f39c4222cad6dcaa6d333efa4f2cfc`  
		Last Modified: Tue, 07 Apr 2026 15:06:45 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d05fa574ca7779186ee850aa2806530f8617f0a02ffc18bb859701aee47e20`  
		Last Modified: Tue, 07 Apr 2026 15:06:45 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c8cd81a472e9def126e3a9bb0ae0317a29ad464fad160ad452e6c5f3090f3275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5231472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab105531560379d8e3983f12b0f2c7ceb86161f8e1a4099848d1c9ec4cbae449`

```dockerfile
```

-	Layers:
	-	`sha256:735b6fe2d4eda47532801a616654956c30ffc0d7da150342fa7a968c599096a2`  
		Last Modified: Tue, 07 Apr 2026 15:06:45 GMT  
		Size: 5.2 MB (5214919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:633a1e035c46be5d33398246764ffede662985768f9aca8ddbe3a3194413a20a`  
		Last Modified: Tue, 07 Apr 2026 15:06:44 GMT  
		Size: 16.6 KB (16553 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:14d4fac3ac2028368ba481310269d2fbb01153a5608d3053c0237ca227ec1eb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.6 MB (192569208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bcfeae71b170c3c97728ff5e892d6dcaff17816ef7961e0ca2a747932b3ce5b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Sat, 11 Apr 2026 22:39:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 11 Apr 2026 22:39:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 11 Apr 2026 22:39:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 11 Apr 2026 22:39:28 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Sat, 11 Apr 2026 22:39:28 GMT
WORKDIR /tmp
# Sat, 11 Apr 2026 23:01:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 11 Apr 2026 23:01:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 11 Apr 2026 23:01:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 11 Apr 2026 23:01:46 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 11 Apr 2026 23:01:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:51128e253868f85aa5e3b9e86448414d946e8a6b685e02db1030aaa2b11e81d4`  
		Last Modified: Tue, 07 Apr 2026 01:55:37 GMT  
		Size: 28.3 MB (28275778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94187439743d0e4ea744bbf1c65c89e279a7b6b83ff5e8684b3251e143001c79`  
		Last Modified: Sat, 11 Apr 2026 22:44:45 GMT  
		Size: 90.8 MB (90773426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322b958ad857d72246cefaf46e881ac5d44f81da21e7df1c6c1e1227dbf789bb`  
		Last Modified: Sat, 11 Apr 2026 23:05:24 GMT  
		Size: 73.5 MB (73518961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:074bb75a180dcf6ed2ed6e3901f2ffcafb1b0c90e734e449b0b8abad36a3590b`  
		Last Modified: Sat, 11 Apr 2026 23:05:13 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad7f1f7e4037a930e852550ee888099424a6f168f92fb296bb9512cb3966717`  
		Last Modified: Sat, 11 Apr 2026 23:05:13 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ab415598a83312be3af58891888316c92173d8a88f493d2ca76f5aa5ac820aab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5215264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bf7cf26acae4e4bc3058ec53a5b44610f1b944d78d74964d04c82eee8b7378c`

```dockerfile
```

-	Layers:
	-	`sha256:6bdb5f48df99d49a718ef91968b70182a8f4dbbb9247ebeaa5fd886cfd708869`  
		Last Modified: Sat, 11 Apr 2026 23:05:14 GMT  
		Size: 5.2 MB (5198711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ce84a26ab69dff1dde1e609c2565c955487d0b6b76bfbeb4d210323621e3375`  
		Last Modified: Sat, 11 Apr 2026 23:05:13 GMT  
		Size: 16.6 KB (16553 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:ca8088305435860f3a5c24015056dc6a0f2ed903f63744336e2cef039efc5ba5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.7 MB (193669091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:859b14ab5e5025f953704af6439f99812b76dd5e677ad23fe5614974aa564b7b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Thu, 16 Apr 2026 00:45:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 00:45:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 00:45:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 00:45:44 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 16 Apr 2026 00:45:44 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 00:46:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 16 Apr 2026 00:46:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 16 Apr 2026 00:46:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 00:46:01 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 00:46:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:82e48a38ec87473a03164a244b5d8dfc2b55ef7a891305e41ee39d937de3c4a4`  
		Last Modified: Tue, 07 Apr 2026 00:13:47 GMT  
		Size: 29.8 MB (29835418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb362cb03216b959febd5e7567d524805fb46e649e271e2b623df3ab0d755a9f`  
		Last Modified: Thu, 16 Apr 2026 00:46:29 GMT  
		Size: 88.2 MB (88233835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1cf27d09061ed701b7e9d1b8c5c657101c7c030cac4a869c710ab8ddcd73a05`  
		Last Modified: Thu, 16 Apr 2026 00:46:28 GMT  
		Size: 75.6 MB (75598793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cde61be10525926e3904b60966569bf0dcc0c15b7df6a67bc313e4c20cc26b30`  
		Last Modified: Thu, 16 Apr 2026 00:46:26 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6efc458dbdabe87ccbeed957e531220612cbb443c20f097c75e0f481bff3bab9`  
		Last Modified: Thu, 16 Apr 2026 00:46:26 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0d05a4a7e82fb886ce5ed052ee414d9c5ace0b620dc7eb49a32d6f0cbffa94b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5224203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7844841470acbd952b1b529e7a8a3004291e2e81e5f4386854c47306e7909c30`

```dockerfile
```

-	Layers:
	-	`sha256:b86cd983c56ed4d2b1da325eff9995e0cfce19705d947c815b6a815d4f487835`  
		Last Modified: Thu, 16 Apr 2026 00:46:26 GMT  
		Size: 5.2 MB (5207710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fe3066c7efe9b0c74086d1e4289648841e431f5becdd385e59fc22ac387b3ba`  
		Last Modified: Thu, 16 Apr 2026 00:46:26 GMT  
		Size: 16.5 KB (16493 bytes)  
		MIME: application/vnd.in-toto+json
