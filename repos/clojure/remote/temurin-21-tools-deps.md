## `clojure:temurin-21-tools-deps`

```console
$ docker pull clojure@sha256:80c7dc6913ef4b2a796ae9e03409f1df3fc746f3c94ba0ee73fc29bd94a07f70
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

### `clojure:temurin-21-tools-deps` - linux; amd64

```console
$ docker pull clojure@sha256:d47fed8490e397b725ef9e4dbf858252743de6493eef6418b525be7dc7e6aee9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.5 MB (287524596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9c5193da3b7b2d148f5caff21ae6c38c3d3d9f26f4eb45ad54e4a41d8491967`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 03:16:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:16:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:16:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:16:01 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:16:01 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:16:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 03:16:15 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:16:15 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:16:15 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:16:15 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d529291d43c8562eeff74b0a53e8617ac925a09966a140c5a596fd7c66c2f49`  
		Last Modified: Tue, 07 Apr 2026 03:16:42 GMT  
		Size: 157.9 MB (157857094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4619fe96b15c29603a15d572dda4820a672537c8fe29a1811201033b27df0e`  
		Last Modified: Tue, 07 Apr 2026 03:16:40 GMT  
		Size: 81.2 MB (81177638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a991b7f0891466eeec9279b2b41f9f89a8256d50a5987e6cf069941013300041`  
		Last Modified: Tue, 07 Apr 2026 03:16:37 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44029d90c5332c8ab8804e12dd96a33dd1b39b248c1654ae0c7d0a0077a1230c`  
		Last Modified: Tue, 07 Apr 2026 03:16:37 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:c4f9d9c41a7a5360e93a4485be01ff21000ef8da671a7d7f057aca2a9b7055b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7397300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c2d1dcefa9f2ebe1f6ed195744f368de323e38945ed832434168fc7e62d7f9`

```dockerfile
```

-	Layers:
	-	`sha256:225af5f07e22edf327705284d3fa75c8a50a457201691f72e01f0000e750635e`  
		Last Modified: Tue, 07 Apr 2026 03:16:37 GMT  
		Size: 7.4 MB (7380838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06b76cb537a298b7f46469dd61ca1cd3c092c0360af74880273e371d6691496b`  
		Last Modified: Tue, 07 Apr 2026 03:16:37 GMT  
		Size: 16.5 KB (16462 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0de4469aa4dfa8df2fbd54c583202d0eb5a2db1f52b5a0155ec84fa7ac961322
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.7 MB (285665638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66ced0f5fa1e1cac1ea4f1c8fdf4ed581dc6f915970b5dba859ac0327eb5be90`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 03:26:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:26:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:26:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:26:58 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:26:58 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:27:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 03:27:15 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:27:15 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:27:15 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:27:15 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249f97a7810f7c4fb76a40f9834ad59904c453f7b015588f06f9cdb000d15563`  
		Last Modified: Tue, 07 Apr 2026 03:27:41 GMT  
		Size: 156.1 MB (156133048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc434ffe318a084c587d54adc25f1b3da1e664c9e9795994d4a3b53db45fb5df`  
		Last Modified: Tue, 07 Apr 2026 03:27:39 GMT  
		Size: 81.2 MB (81158285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3072b97b5dff8a72c0354b5c33eaf8ed06019f8c1960459132949519b4480daa`  
		Last Modified: Tue, 07 Apr 2026 03:27:36 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd8c7f8c89d0d3fe2c294e8858fb6ae0cb5ab846ffa026ab5037f88998b16225`  
		Last Modified: Tue, 07 Apr 2026 03:27:36 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:a139e81e64c441a46342ad8d87c31922575d99fbe54e7f3a1151feee432ce7cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7403229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:218274f2df53422fdec2ecef906a8c6e76ebafb9f62f7c9d2a388dbd26232da7`

```dockerfile
```

-	Layers:
	-	`sha256:87175d95d93a825ab235de5da4605841b29ee3ea2a22131ffd468f3cdc420114`  
		Last Modified: Tue, 07 Apr 2026 03:27:36 GMT  
		Size: 7.4 MB (7386625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23449a86138e7f2a4227a2ec0d3fa203f03676cc76a33ee1f0ed4de8aa7aab6c`  
		Last Modified: Tue, 07 Apr 2026 03:27:35 GMT  
		Size: 16.6 KB (16604 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps` - linux; ppc64le

```console
$ docker pull clojure@sha256:c9c2b870ba383391ca3fb9a2cd752f1a5b812bb06e1561706a30505af0148353
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297315768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e78eb949e118d849d28aa8af9d1eb0aa485a65776b7ea096527542a76f0fc603`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 18:34:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 18:34:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 18:34:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:34:34 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 18:34:34 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 18:40:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 18:40:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 18:40:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 18:40:14 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 18:40:14 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c072e92b832614e86d956c6381c6b7617944feae3193ea5691e9506870844136`  
		Last Modified: Mon, 16 Mar 2026 21:51:19 GMT  
		Size: 52.3 MB (52336698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45fbb79ec0e62d97d7f7a307c9ff90dd94c14b4ef06ecb05232fe909cb1db302`  
		Last Modified: Tue, 17 Mar 2026 18:36:06 GMT  
		Size: 158.0 MB (157977514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837d0776d8827c11d836a36d861a0da2828640e3724cd60110bf6cf81ee3b40f`  
		Last Modified: Tue, 17 Mar 2026 18:41:02 GMT  
		Size: 87.0 MB (87000512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca536a2d7f4e827ccc9ba9609ca6b47e0afae8d67c1e5fd6930dd3dc6a6a918`  
		Last Modified: Tue, 17 Mar 2026 18:40:50 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a954452be50da89565671c5e7fbe8b6ccadf6901a54b9b1922c9597c730840`  
		Last Modified: Tue, 17 Mar 2026 18:40:50 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:516aeda072d215319a53c647563b555d9d227ca6741025e7a5d508326f4d3945
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7402588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38bd51d51e33955c2df2504ffed8932a0a9eb21dc66bfb9473a531160a437498`

```dockerfile
```

-	Layers:
	-	`sha256:6362abfb0ff13504a5db234a609d1dc919e20875c39eb1490ce9bc495c2c1579`  
		Last Modified: Tue, 17 Mar 2026 18:40:58 GMT  
		Size: 7.4 MB (7386066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c846ba22516708c40f62f1b54504c85b1318c402434663d93744c52df552424f`  
		Last Modified: Tue, 17 Mar 2026 18:40:56 GMT  
		Size: 16.5 KB (16522 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps` - linux; s390x

```console
$ docker pull clojure@sha256:59c4590c29425589251ee56d2a282b48f4ab630d99656b77eb8ba1420c078f33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.2 MB (274242416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8fbc4484c0bae0164309a29b577135aac1b9b98cb08fe6622a848d7186f9b07`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 05:45:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 05:45:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 05:45:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 05:45:16 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 05:45:16 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 05:45:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 05:45:30 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 05:45:30 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 05:45:30 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 05:45:30 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:40ecbf1d4e17f6b072e6cef463823baec601d9f21c9dc33d98bd258448a986f6`  
		Last Modified: Tue, 07 Apr 2026 00:10:32 GMT  
		Size: 47.1 MB (47148084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa37d5d2197c3cb308ae61c0aee840666757f96b738357351f34685c9b11dae0`  
		Last Modified: Tue, 07 Apr 2026 05:46:02 GMT  
		Size: 147.1 MB (147105213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab8f70c91ea80705dcf858669d0f675b0b9e7da6dd566071761ea8225cbf07c`  
		Last Modified: Tue, 07 Apr 2026 05:46:01 GMT  
		Size: 80.0 MB (79988077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb331fcefbe6696e48c23962bee8fd99353f65bd608183e1c44aac8a24fe3c9`  
		Last Modified: Tue, 07 Apr 2026 05:45:58 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8350dc513b6067d393b39b3859d221f1095542fa2b18fa20f89caf269df2e8c`  
		Last Modified: Tue, 07 Apr 2026 05:45:58 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:c9036463172a974ab2d3de77769a0805fd4320e11926f34676c1b76723621622
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7388619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3195ee98f50f328022f48cd5b304de4192ac3ae090dc546145d1f4a2d12a4391`

```dockerfile
```

-	Layers:
	-	`sha256:f797e0982dcee58776d6355266d5128b5e99ddad2ddec7e426c53e151433a86f`  
		Last Modified: Tue, 07 Apr 2026 05:45:59 GMT  
		Size: 7.4 MB (7372157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8d6c4f8c78254988abcabc2e8fc3f8d9e53fdb55bccea4d3bc5f5824b755c7d`  
		Last Modified: Tue, 07 Apr 2026 05:45:58 GMT  
		Size: 16.5 KB (16462 bytes)  
		MIME: application/vnd.in-toto+json
