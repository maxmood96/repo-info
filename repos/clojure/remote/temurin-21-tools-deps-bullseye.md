## `clojure:temurin-21-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:c6b4054ea9844aaed13f66707f9f721b535e1a468fbeff4e27bdca7d02104538
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:52178d18d6c55e9e90d6a99735dfaf71186d167f159f828fde338ec7991a5703
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.2 MB (281222177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5ab8d36b5608409e5d16d2e1e063679f46f61875a481e89c53f3438bde79f74`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Wed, 15 Apr 2026 22:05:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:05:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:05:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:05:34 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:05:35 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:05:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:05:47 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:05:47 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:05:47 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:05:47 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ced3088fc7691915325d6187786ba346149f7c9dcdbfb3772ca71be74bf87622`  
		Last Modified: Tue, 07 Apr 2026 00:10:43 GMT  
		Size: 53.8 MB (53762793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aea1c958306437d2e64d9a5f798807b2022ef12523751bc1470882dcbd1a876`  
		Last Modified: Wed, 15 Apr 2026 22:06:11 GMT  
		Size: 157.9 MB (157857060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c621019ce68045f12d7270cb58dabe36d1f89b738543ea29f32255483fda8e7`  
		Last Modified: Wed, 15 Apr 2026 22:06:09 GMT  
		Size: 69.6 MB (69601283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc80366dc12d99138ac929c7223b85988a46e13fc386764c265b893ca1bb6bb`  
		Last Modified: Wed, 15 Apr 2026 22:06:05 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eadd6e2b458a652acc376996303aa9e3dd10582625a2577298e923e233684058`  
		Last Modified: Wed, 15 Apr 2026 22:06:05 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:8eaf916bb7bfffe3c007da6191e5ad0ab17cc9af99457aff31d2914e3d0167dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7425283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f14d1f0bead1afdd449f7427cc1927b5b5386138300a01a001cff451260b72c7`

```dockerfile
```

-	Layers:
	-	`sha256:f56f3b9aa5f959667778a04f93a63e0aabf712c122218536ee439cc3c0445e8a`  
		Last Modified: Wed, 15 Apr 2026 22:06:05 GMT  
		Size: 7.4 MB (7409505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:676d9b757fb5930d92268ad3a135a8933f4254e22dab3da3ac1b19498c71afbd`  
		Last Modified: Wed, 15 Apr 2026 22:06:05 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f29bc61b04705112282e7ae77faa05028fb3d20769110963a6123ea1df2581d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.1 MB (278125756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bf87848b9bab6bf57e7ef23a860d8a6a13c06d37fe999f86fa98f40e2f47e08`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 02:22:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:22:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:22:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:22:56 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:22:56 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:23:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:23:09 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:23:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:23:09 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:23:09 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d66293db501a72163d605baf6b3e8451c38d0fe30b934c24cec53a4e66b6e46d`  
		Last Modified: Wed, 22 Apr 2026 00:16:07 GMT  
		Size: 52.3 MB (52253001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3903b6435013c6df9ac7fd65d3f4f76e4ea618ecc0e9d18657ece81297b8b311`  
		Last Modified: Wed, 22 Apr 2026 02:23:33 GMT  
		Size: 156.1 MB (156133044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed52a1b10ba6167b2d30061be6250d46c7373308d8b7087e0f456c3ec5254506`  
		Last Modified: Wed, 22 Apr 2026 02:23:32 GMT  
		Size: 69.7 MB (69738670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0ca895d9b42919223a462186ee1de0d706c9a51f94cd217511f438cb84b886`  
		Last Modified: Wed, 22 Apr 2026 02:23:27 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62cc17fc7a3b077325ac0e90e4383b0911453cf50df97052fc95c85e1152d9a4`  
		Last Modified: Wed, 22 Apr 2026 02:23:27 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:2c80623c5d8e9f51c93113513d83c7089dd01a8dbbe2371b548bd6af9cdfe284
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7430499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3981648c660dc4b5442ea8a078497b4193ca36f1f377b75a4748ace054773686`

```dockerfile
```

-	Layers:
	-	`sha256:d49eaecbac76c8c3472402fc5153000f19ae55a46eb051e26aa2f2038fa120be`  
		Last Modified: Wed, 22 Apr 2026 02:23:29 GMT  
		Size: 7.4 MB (7414604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0b7258ba60a11ad704346e0a8a519f3513b081f91afda48db022ced4d2ee17c`  
		Last Modified: Wed, 22 Apr 2026 02:23:28 GMT  
		Size: 15.9 KB (15895 bytes)  
		MIME: application/vnd.in-toto+json
