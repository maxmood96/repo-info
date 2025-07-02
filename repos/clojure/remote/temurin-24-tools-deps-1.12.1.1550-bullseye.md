## `clojure:temurin-24-tools-deps-1.12.1.1550-bullseye`

```console
$ docker pull clojure@sha256:c7a6665d16160bd7f85443d62e69387afb946d6c3502095ab7c0f50fac32575f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-tools-deps-1.12.1.1550-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:e2c7315df1dd6609b30199b0c6c9a27c6918da358cd266e659b5686362aef43d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.1 MB (213117701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44892a53b99134fbbdedd294d9f911ae518fadc9de8e235f441d4c1fe5a3ab54`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
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
	-	`sha256:2d765646d883a37610a09973a079fbba4c7596e54d18d0447bdfff142389d1f7`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 53.8 MB (53754822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f239cb83a22bdc6a514ec363bf1e5ee9688fab250495fee990d452270fb7e4fe`  
		Last Modified: Wed, 02 Jul 2025 04:17:44 GMT  
		Size: 90.0 MB (89952014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:511d03baa4669006e349e71ded2731139660cfb9d0659010a62741693bed802e`  
		Last Modified: Wed, 02 Jul 2025 04:17:52 GMT  
		Size: 69.4 MB (69409828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41cec621cdeb06eb53315e91938444a461afe2fe2eb9dfcdbaff306ef6294d63`  
		Last Modified: Wed, 02 Jul 2025 04:17:26 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f780a282139d4b2444baf216714d345e77db9265ec7ae7be7fcb0000e791192`  
		Last Modified: Wed, 02 Jul 2025 04:17:26 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1550-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:bb3618dfcf39f6194bf0b4d85d6aaca6720de49120d7251ce604c3de5e10aa39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7362098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b05f58518866c2a48d194953d674dc82e8aa4b04dfcd7f8ee4136ccc1a6a59`

```dockerfile
```

-	Layers:
	-	`sha256:69fc5a9968baae4e442136fa8b7e43450302e611cf5b9820f0466d63feffb838`  
		Last Modified: Wed, 02 Jul 2025 06:41:07 GMT  
		Size: 7.3 MB (7346284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2092ebaf3cb7cd1c643ac7bc1c85f6dfbc7030e20e598874dfe4d118f040da81`  
		Last Modified: Wed, 02 Jul 2025 06:41:08 GMT  
		Size: 15.8 KB (15814 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.1.1550-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:54e274e26da6f5c39f3c2814976ad3e66641e5e605d5e6cedad5cffaea070e98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.9 MB (210882101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c728af87dd0c6b8c2fc6e4c78f485fcce535d0acb0c536ece4be5f6e21d63f1e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1751241600'
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
	-	`sha256:df45b4853b6fce6b81d1ac6218d861c6d7c8c14da4be409d42ee4bfdf0737e71`  
		Last Modified: Tue, 01 Jul 2025 01:15:18 GMT  
		Size: 52.3 MB (52252254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8ac54386d4a9338c8561508d35cc624efee0d661ad8cdd0ddcca4d5714029e`  
		Last Modified: Wed, 02 Jul 2025 12:56:57 GMT  
		Size: 89.1 MB (89091234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9830ddb42b1af437f64465a9d7a0c915c5d200679adbf59ae928f7aa7cd5451`  
		Last Modified: Wed, 02 Jul 2025 13:02:25 GMT  
		Size: 69.5 MB (69537571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c37802d3844e9b6533a16c7996e816273ca17eb8e68ba8fc8f9f02e65ca4ea`  
		Last Modified: Wed, 02 Jul 2025 13:02:22 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da66ae409a98114100be0b04cb69c603b343815de31b11e74c5584107cc1df50`  
		Last Modified: Wed, 02 Jul 2025 13:02:22 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1550-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:433b481ae28a0be09fae1ecd4a0d56e05b2b0d8f5acfea8b155ba1b1a57fb770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7367312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86964f00abe97a73716e19b8b345df0d15b9a0fcc47f6edf3787458bfeb1cac`

```dockerfile
```

-	Layers:
	-	`sha256:ade4e0603c5213460a1934bc20831727831a3666df573f0b525f2290b433b2f9`  
		Last Modified: Wed, 02 Jul 2025 15:42:00 GMT  
		Size: 7.4 MB (7351380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dce25c5c3e1cb761cdba982c483665ba2f68df69d3c551764c4077e00c1144f`  
		Last Modified: Wed, 02 Jul 2025 15:42:01 GMT  
		Size: 15.9 KB (15932 bytes)  
		MIME: application/vnd.in-toto+json
