## `clojure:temurin-21-bookworm`

```console
$ docker pull clojure@sha256:f40737e5ba5b9f235b68579bbefd54780a69713afb54443d9e935cb14dde617c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-bookworm` - linux; amd64

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

### `clojure:temurin-21-bookworm` - unknown; unknown

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

### `clojure:temurin-21-bookworm` - linux; arm64 variant v8

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

### `clojure:temurin-21-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:98eda92cee2d1c92fb44c61c49675c1910c93f713adeb0da3051c7889256aa99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7201424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91f64cb873617268a078a2598ea78fa3ea16bdb379f2cee931b30106399b5a28`

```dockerfile
```

-	Layers:
	-	`sha256:8b04429efc96c9f57a9720a66344b2dabf37f2e2e7856368749cf1eaaf8aeab2`  
		Last Modified: Wed, 30 Apr 2025 01:44:57 GMT  
		Size: 7.2 MB (7183413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:182fc0e9fb9f324ce2023302188c676658ecf467c825fdccd908dbf97b593c80`  
		Last Modified: Wed, 30 Apr 2025 01:44:56 GMT  
		Size: 18.0 KB (18011 bytes)  
		MIME: application/vnd.in-toto+json
