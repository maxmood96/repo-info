## `clojure:temurin-21-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:be2b9a66454d143503e1f8d44e9de6bc91c1e1e40c597bb2331ccb2e3f43823d
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

### `clojure:temurin-21-tools-deps-bookworm` - linux; amd64

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

### `clojure:temurin-21-tools-deps-bookworm` - unknown; unknown

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

### `clojure:temurin-21-tools-deps-bookworm` - linux; arm64 variant v8

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

### `clojure:temurin-21-tools-deps-bookworm` - unknown; unknown

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

### `clojure:temurin-21-tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:720039d0ee1924c0ce6f73be13cf5fc04b9cd73dda2b20f123a447a1a1b6d36d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.9 MB (296938623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66eb7b84179a27dff1636ffb5b5dca39535c2582ee2530543970f4b3b6f3c30d`
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
		Last Modified: Mon, 28 Apr 2025 21:21:34 GMT  
		Size: 52.3 MB (52332129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2bc318831ce756576c268e9599222761fdf41dc94981f81f41b532a8b7e7e22`  
		Last Modified: Tue, 13 May 2025 17:55:11 GMT  
		Size: 157.8 MB (157804906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e2881473afb93a309b45e7e901091230e378c7f327a66237ac2a00fa40a8a3`  
		Last Modified: Tue, 13 May 2025 19:20:47 GMT  
		Size: 86.8 MB (86800546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ebd6b4d18d5cd14c4299684b53f831bb7bf7f1fb6d637b2655d5698c0d566c`  
		Last Modified: Tue, 13 May 2025 19:20:44 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc07670309152a23b30266e4291dae7e6212840c1bfe809760fad96dad9a38f`  
		Last Modified: Tue, 13 May 2025 19:20:44 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:530dac63eb6a539e334f56e203faa1742577500037f164ae8a2812b8348afa8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7200561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5d6630d610dcca7958e9bfd8cb3337b2554c9b9f34be0ea1a67d477e4372f58`

```dockerfile
```

-	Layers:
	-	`sha256:e29dde749e47838773b8aa1e4e66fb8888767b177a7433906345c7ddd87df081`  
		Last Modified: Tue, 13 May 2025 19:20:44 GMT  
		Size: 7.2 MB (7182656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b2152386538f966ee3589a97e478ca204d942e80d8e1247cc49bc39fd37a9eb`  
		Last Modified: Tue, 13 May 2025 19:20:44 GMT  
		Size: 17.9 KB (17905 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:46f6607dcae1b0cdb7043d29bb4a92b8331ae7d4724b07caa3c2d4339493ccb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.9 MB (273859967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f8356523039e076dbff3c27b7061eb119f8c2e39f09774ec0eed725e6490040`
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
		Last Modified: Mon, 28 Apr 2025 21:07:54 GMT  
		Size: 47.2 MB (47151332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe961db0a5b8a3d7370d66b20b0d0b677ced354a7253599211f0ea8053e5454`  
		Last Modified: Tue, 13 May 2025 17:54:32 GMT  
		Size: 146.9 MB (146910920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e3f224b886431a7e1fa00cb790e6c8114650f03c39feb5110a8abf00a533e1`  
		Last Modified: Tue, 13 May 2025 18:27:32 GMT  
		Size: 79.8 MB (79796676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40050b91e1256547e44e8ca868e7520437bb479333d02e225872748e23158b20`  
		Last Modified: Tue, 13 May 2025 18:27:31 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2432d299d4dbab041de03b966b18e22aacca4dd65652956a9a07a81f06c7b3bb`  
		Last Modified: Tue, 13 May 2025 18:27:31 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:d83728bbe26a862a5886db0ffa254d762e1e5b9ab969e272caa5d6b05ef3f084
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7189610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e8cf63495460f9865386279b58efab6cf4df67b068038ce9c16f9ebd2c52638`

```dockerfile
```

-	Layers:
	-	`sha256:8656d29604957b3beb7b348e67fb1aa311350c04dcdd146395e991369b38a6df`  
		Last Modified: Tue, 13 May 2025 18:27:31 GMT  
		Size: 7.2 MB (7171789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c3f0c759790680ba0bed34360eaeae321750003943a59142df9187969f48ef0`  
		Last Modified: Tue, 13 May 2025 18:27:31 GMT  
		Size: 17.8 KB (17821 bytes)  
		MIME: application/vnd.in-toto+json
