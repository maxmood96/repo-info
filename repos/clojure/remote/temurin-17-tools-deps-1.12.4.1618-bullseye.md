## `clojure:temurin-17-tools-deps-1.12.4.1618-bullseye`

```console
$ docker pull clojure@sha256:e0fabc24c170d9821fb85e1ab258ef19e3438c03077fb5166f2a703f00f5aa79
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.4.1618-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:d0c89015fb957199f9884dc54d5234f09ee4665b30f6d5487e02e0b51e826fbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (268993747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01d74f24f8f32e4f362da8b5cee804ec708a02892fa8491f5bc6448885d9e808`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Wed, 15 Apr 2026 22:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:04:12 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:04:12 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:04:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:04:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:04:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:04:26 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:04:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ced3088fc7691915325d6187786ba346149f7c9dcdbfb3772ca71be74bf87622`  
		Last Modified: Tue, 07 Apr 2026 00:10:43 GMT  
		Size: 53.8 MB (53762793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5335b8f1080433f4c9c97ae22e6235ca7679f8bde54d2cbb531f01ac91bbebbf`  
		Last Modified: Wed, 15 Apr 2026 22:04:49 GMT  
		Size: 145.6 MB (145628767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb2910d6288611fc712376d729e62fc68568444268ec13067bb0a12ceba420e`  
		Last Modified: Wed, 15 Apr 2026 22:04:47 GMT  
		Size: 69.6 MB (69601144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06c9e3ccbaf22cffc4ab38607cce2b74729950702da1b4c9c73fefdf64eb33a3`  
		Last Modified: Wed, 15 Apr 2026 22:04:44 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b525f775998888a24a55714cd7500ca3e8f94b106eb9fc054a5921b4bfd539`  
		Last Modified: Wed, 15 Apr 2026 22:04:44 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:c3d34ae6756c9a828a076ef9e6f0e783e9ba69c9de26ed6dbce068f1eab24636
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7423430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f584b01ebf87f24f55ef1748e4c7ab196018f517350a82fd4ecb918c369b1202`

```dockerfile
```

-	Layers:
	-	`sha256:0cb1edb88ac416adfc3610a83d9464a14b83b8eb371bb59770a5d089e13ddbce`  
		Last Modified: Wed, 15 Apr 2026 22:04:45 GMT  
		Size: 7.4 MB (7407653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b20b99d1347ddc28ed8cd711414e008273e1df061f1bb33140235211b5e5691`  
		Last Modified: Wed, 15 Apr 2026 22:04:44 GMT  
		Size: 15.8 KB (15777 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:819b3753c96a25c8cf2c9cb893afced31b6b53b42d95432696e2697411710a2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266412965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe7eddb70d1714354701f546a64a192735bdb0479f3fc3992f4b034643c4de48`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 03:25:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:25:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:25:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:25:48 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:25:48 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:26:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 03:26:02 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:26:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:26:02 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:26:02 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:910d955c4ed64a8ee0854ded27fe508086448dca2dcf21a0af023b8bc9d2020f`  
		Last Modified: Tue, 07 Apr 2026 00:10:48 GMT  
		Size: 52.2 MB (52247615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8590ed84aa3e84810beac71cabfa9a3144347a276e61a9e6518b71511f17e381`  
		Last Modified: Tue, 07 Apr 2026 03:26:25 GMT  
		Size: 144.4 MB (144436252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4fc513df70f3b0e09a540141d8c9176d9bbb68347cc3a31c473bdc733fe600d`  
		Last Modified: Tue, 07 Apr 2026 03:26:24 GMT  
		Size: 69.7 MB (69728058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0568f085846f892f492ffdc62a09a8df92d8d405140eeaf7c913e4eeab6a7c75`  
		Last Modified: Tue, 07 Apr 2026 03:26:21 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84156afc79b4dd882ae9930332791698af64887ca046bf2a06825cbb92ccbdb3`  
		Last Modified: Tue, 07 Apr 2026 03:26:21 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:8bade938991c806209cf4c1f86ab11e838493eb319b2e7ac80da4628e8f95e40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7428648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:817fbec6b50282d8f1690eb626ff18e9d2b58ea145b79dad1bcfc7bb89855b40`

```dockerfile
```

-	Layers:
	-	`sha256:e94265080b84681476e39e6d1e09c39179eff1f1bc7333a2b7536c94c10ae1f9`  
		Last Modified: Tue, 07 Apr 2026 03:26:21 GMT  
		Size: 7.4 MB (7412752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:344ce90803b3e53aa314bcfde76102d1c2bf5622fc102fd9c451327e89cbcb34`  
		Last Modified: Tue, 07 Apr 2026 03:26:21 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json
