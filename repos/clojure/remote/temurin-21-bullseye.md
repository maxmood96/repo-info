## `clojure:temurin-21-bullseye`

```console
$ docker pull clojure@sha256:b7aa4c1d6247363240a6841eb61ae6dc8fb4f0b4cd2304b5f95861e316ef0a0c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-bullseye` - linux; amd64

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

### `clojure:temurin-21-bullseye` - unknown; unknown

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

### `clojure:temurin-21-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3d29cff38b5ce9b97d14d3a489eb63de429ebd5843df3832c54ca7f66c4bb772
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.1 MB (278117871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9c1e3c7311c251613b6bfd93a6d7e23b15ef89a23f71949900fcc3d7468eb0d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Wed, 15 Apr 2026 22:17:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:17:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:17:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:17:02 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:17:02 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:17:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:17:17 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:17:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:17:17 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:17:17 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:910d955c4ed64a8ee0854ded27fe508086448dca2dcf21a0af023b8bc9d2020f`  
		Last Modified: Tue, 07 Apr 2026 00:10:48 GMT  
		Size: 52.2 MB (52247615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd0be9da07319a7ecc84b540b020dc3da3659f3291a56858eb98793a9a1d5a6`  
		Last Modified: Wed, 15 Apr 2026 22:17:42 GMT  
		Size: 156.1 MB (156133057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00dc1cfdaa7b82bc7481195bb0a35d260dad31306f9d0de43d6fc1e94e22147`  
		Last Modified: Wed, 15 Apr 2026 22:17:40 GMT  
		Size: 69.7 MB (69736161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff7276b961f4103218defe444071e4fdf071ca8bbe06afc018aed91a31bea65`  
		Last Modified: Wed, 15 Apr 2026 22:17:37 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27cc11237a9f8d38ab3befa52a3f1b0b2b433cdf7a8fd42213d8f50f1e9377b`  
		Last Modified: Wed, 15 Apr 2026 22:17:37 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:6254f78cffabb1b6aaf4632ae57137d8138eddd9d0c994c93d99825a345fb4f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7430500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2898bb4061e37531cd138d466b1fac50f6329f52ffe3cf731fa792f81af5c6be`

```dockerfile
```

-	Layers:
	-	`sha256:11ea203a15ae5bf93365a73c9cb53b38cf79d0bf9b7abcac20a07148369f962c`  
		Last Modified: Wed, 15 Apr 2026 22:17:38 GMT  
		Size: 7.4 MB (7414604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45e5a8957e7fe394778bb54ec28b0c88d7d97abc7ee8cebe7ade435c5b9e63d7`  
		Last Modified: Wed, 15 Apr 2026 22:17:37 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json
