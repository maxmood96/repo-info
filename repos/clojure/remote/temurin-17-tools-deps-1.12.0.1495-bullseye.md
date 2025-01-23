## `clojure:temurin-17-tools-deps-1.12.0.1495-bullseye`

```console
$ docker pull clojure@sha256:c26e8531bb4a65fafedacfa0dd5e1164c0e74f57e4f583083f6e1137a64a0f9e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.0.1495-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:f028b331f56ea362c52cc38c9c67bedf975cc6cb179453440dcc79183c3aee2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.5 MB (267455424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6735125ca4f6e77180adb84fec1ed63845326eac0169aac6e2d33e0cd4e863f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:de97e8062e06250e3c3cef0d40cfe62111bb4b74bcf6221e25a06452dacffcf6`  
		Last Modified: Tue, 14 Jan 2025 01:33:36 GMT  
		Size: 53.7 MB (53739164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94c0fd9204bb07d06c249dd4e836423788f666bbfe6980ecff000979906e8c1b`  
		Last Modified: Wed, 22 Jan 2025 19:37:00 GMT  
		Size: 144.5 MB (144536747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9571b0bde8969cf525ccb815529b2c67faf6ec6a74d3c85b45485a6a19ee49d`  
		Last Modified: Wed, 22 Jan 2025 19:37:00 GMT  
		Size: 69.2 MB (69178469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cac30e23f6ebeeb3738ee9d26670ca14302de6fe3eb6ff451a0152cb7f26338`  
		Last Modified: Wed, 22 Jan 2025 19:36:58 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0b77c90a89d06adc6eab68606dfde315dfe6b8dca3db6d05f0ade49a4a0115`  
		Last Modified: Wed, 22 Jan 2025 19:36:58 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1495-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:3f31cd7079af6d8d20ffea4d292db3835b27ae217ba97aed44262a76d6c91ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7220377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc3b02b975d59a39c294be4d6eaf8b57132e3ab3bae79a2b981dc10497e0b984`

```dockerfile
```

-	Layers:
	-	`sha256:e7f645b2266f266d9f863704f644298aec8b2145b02d46c006539ec002ce37ce`  
		Last Modified: Wed, 22 Jan 2025 19:37:02 GMT  
		Size: 7.2 MB (7204557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05543cb6a2f436f15835ac1e2be43820d269383c5d0a815877d6c026fdbac220`  
		Last Modified: Wed, 22 Jan 2025 19:36:58 GMT  
		Size: 15.8 KB (15820 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.0.1495-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0930458c96169059c9b14cc8ed17754c78ce2a159e32cfe8d70d29d8ac3ae52b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.9 MB (264912566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28476598da7499c6e8bbea902a6cf7ea834b63c85ab2b1de96cf658566c96e15`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1270858b2b9cb5d47abd119b946534b70ff7d09f29c425fc07b280e5c28971c6`  
		Last Modified: Tue, 14 Jan 2025 01:36:12 GMT  
		Size: 52.2 MB (52246060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c6294b66545c2106d91b39f87bb956189502ec9906cf30f827d89749a1780d`  
		Last Modified: Tue, 14 Jan 2025 12:28:41 GMT  
		Size: 143.4 MB (143360959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3abece7778db9022b8dfadccd0610024b92c18c44f16f4f551ceb51c80f38b3`  
		Last Modified: Tue, 14 Jan 2025 12:31:45 GMT  
		Size: 69.3 MB (69304508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7213d26c643113b3fad6813e5975b5d09f256807c56b5be23a3a0147b3897c1b`  
		Last Modified: Tue, 14 Jan 2025 12:31:43 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bfd92cd8a3c513b0078181ff0868f9f734c3e5f92c539e1e9e775dca8b93ebd`  
		Last Modified: Tue, 14 Jan 2025 12:31:43 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1495-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:58ee2000a8709b5af6ccd854b5e94429dff0dd1a3bd6c9369c14a3754fae8142
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7225595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:454addae052a68b7f4b5bd8b22a322b0a81b9002eefb17d39c3bf322629aeed5`

```dockerfile
```

-	Layers:
	-	`sha256:7406771723a973a2821905a72050b3b3d213867e911f8becb4333f449c980002`  
		Last Modified: Tue, 14 Jan 2025 12:31:43 GMT  
		Size: 7.2 MB (7209656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ddc5a2f5ef342209598d4f1433cb09979ff7ae7e13e3adc22a5fa3aee9ec22c`  
		Last Modified: Tue, 14 Jan 2025 12:31:43 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json
