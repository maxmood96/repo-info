## `clojure:temurin-17-tools-deps-1.12.4.1618-trixie`

```console
$ docker pull clojure@sha256:1d80ca531717840b25a958f26bd2ea4767213ba6b469e23ae42b90b11bd99489
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

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:cac6b8c81a59b65c7fb99116b8103490923a50fb3043794938e644735b7b0537
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.5 MB (280494230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acb5041252c4bbb1c99fcd938cf598d67c72badbde1f9f8421b567f0590bab96`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 02:58:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:58:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:58:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:58:44 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 02:58:44 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 02:59:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 02:59:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 02:59:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 02:59:01 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 02:59:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8f6ad858d0a46fa8ee628532c70b8dc82d06179d543b0b09ec19fc03d4c5b373`  
		Last Modified: Mon, 16 Mar 2026 21:53:17 GMT  
		Size: 49.3 MB (49297530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94abf4187070857e834be97b2bead1c38b1a3c811318510c69725cb686ba9f7f`  
		Last Modified: Tue, 17 Mar 2026 02:59:26 GMT  
		Size: 145.6 MB (145628435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa2dd57aa48f7fe671b969de6c98b0d21e2b4c84b8e7eb009819d49e4b42575`  
		Last Modified: Tue, 17 Mar 2026 02:59:23 GMT  
		Size: 85.6 MB (85567227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e459819902b395adbd86adbb59c597b6f6d51f7ad42aae4106215f666008da50`  
		Last Modified: Tue, 17 Mar 2026 02:59:20 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696afd42beb05a4c6644a3501bb10b460f75fdc3cc4d15f5a50e2cf7b7b15a78`  
		Last Modified: Tue, 17 Mar 2026 02:59:20 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:af3632df23a205103627abe198b72640705e992960752e4005175a04ba85fdb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7486421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b13c03e0fca502c0cf1942d4121c04dd588a1d632719817e6b91b39bcf1e685b`

```dockerfile
```

-	Layers:
	-	`sha256:55ff943ebc9d7132be9d7954564f5daa0cb77a5760d1f0468c96efe5a49f4778`  
		Last Modified: Tue, 17 Mar 2026 02:59:20 GMT  
		Size: 7.5 MB (7470667 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebb06e7ab519f62e788c23801da1ed68cc69ad7dbb1f96430f725b9658f71ba0`  
		Last Modified: Tue, 17 Mar 2026 02:59:20 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7a12f4abe6c5f1bfe30978b7462bb736c8e3a72fdc53d0b529ba99a83445af42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.5 MB (279485421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83393bea52a34bf00881d30fd7096fc5901fc938dbe2e11b71e94b4609c0d5ae`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 03:03:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 03:03:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 03:03:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:03:29 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 03:03:29 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:03:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 03:03:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 03:03:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 03:03:48 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 03:03:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:deab8db42772fcfeb45003461fe0eb7bf63bdb29199a4fb76242b9493437c28b`  
		Last Modified: Mon, 16 Mar 2026 21:53:03 GMT  
		Size: 49.7 MB (49664953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc4d20db6a99cecac94193b1848be4ed2d9a1630ea0fe32bdf8ab2ee66497bb`  
		Last Modified: Tue, 17 Mar 2026 03:04:13 GMT  
		Size: 144.4 MB (144436241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e9ea94e394271119478116dff787271fe37dee113b82f89f30476d137f9f160`  
		Last Modified: Tue, 17 Mar 2026 03:04:12 GMT  
		Size: 85.4 MB (85383186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c59d196d85255586fa2917637592f591d043fcf526e63820486abdc852025b4`  
		Last Modified: Tue, 17 Mar 2026 03:04:09 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e770d00dfb7ea79b8b91a3e5132cd49232479022299073cc1130f73c33c6c7`  
		Last Modified: Tue, 17 Mar 2026 03:04:09 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e279198814f72a34e603ccbc353965ad6eb7f7ec7f62c6987bc90c4d94353db8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7493569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16507af1823a277744bfe0a7bed3d076b9e9c6a4c1b1bc7fd1077ad55018542d`

```dockerfile
```

-	Layers:
	-	`sha256:1362eb6235b00f001e27bc785039b6241825a32581fd50d310ad08cbeba6d4a7`  
		Last Modified: Tue, 17 Mar 2026 03:04:09 GMT  
		Size: 7.5 MB (7477697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4eb712feb0032c60412e09bc47d4eb8d45d131847b93d339437fb73d115800b8`  
		Last Modified: Tue, 17 Mar 2026 03:04:09 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:ea85fe358485cdf7cc3aa12379a656105a390030049bb22788583654b274dffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.5 MB (289544935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8c909ab2b75ae9472308f5002d4194e8b7359342e6740a7805a7f21645e66bf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 18:27:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 18:27:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 18:27:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:27:35 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 18:27:35 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 18:33:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 18:33:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 18:33:38 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 18:33:38 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 18:33:38 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:616ed6c40b4f1136ebcda954e46e021bcee567aad248468321da4f4065f4a14d`  
		Last Modified: Mon, 16 Mar 2026 21:55:32 GMT  
		Size: 53.1 MB (53118350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:822c66d457280a71230ad4487fd70323ef90d3d8e95b8850297f2bd84ecbef19`  
		Last Modified: Tue, 17 Mar 2026 18:29:06 GMT  
		Size: 145.4 MB (145438236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5cc19bef13ae96c0db875f9ffb4a98f1a658a98ceb3f505616c3924652dccec`  
		Last Modified: Tue, 17 Mar 2026 18:34:16 GMT  
		Size: 91.0 MB (90987307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5fa96209f5785aee388bd7f46c3e7c35f19f697cbd57036f3cb442ea75ec434`  
		Last Modified: Tue, 17 Mar 2026 18:34:14 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:981e429fbe00995188a27439e4540d4fdba8fbafd17798be12f36146b7e9d06c`  
		Last Modified: Tue, 17 Mar 2026 18:34:13 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:c7f16750d009579c6117a3b8b0fd4b1b15c44b1131a7b702aa0942b37426e5c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7490890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5de498a0417d403aed543dcfab76f5e6e5c3f01d0cd051e982f9f403a456ce3`

```dockerfile
```

-	Layers:
	-	`sha256:18b363d2f04bf96bdc30b04933ea5ddafbbd0d6291ea1c75f344ddbff0bf6776`  
		Last Modified: Tue, 17 Mar 2026 18:34:14 GMT  
		Size: 7.5 MB (7475088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89322619e4e6586a48c7f7d0880d50eb3a5c5faf74910535fe4843c314f9cb06`  
		Last Modified: Tue, 17 Mar 2026 18:34:14 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:b33e1ee4a6c9da0dc71ac96a98f92c5b8d8ee9b405fc175462c866b6717b50d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.9 MB (274915328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b63e01ee344b7ed34b37109c8511696f150370dedfbce474d752f6f70b3d81d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1773619200'
# Sun, 22 Mar 2026 18:22:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 22 Mar 2026 18:22:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sun, 22 Mar 2026 18:22:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 22 Mar 2026 18:22:07 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Sun, 22 Mar 2026 18:22:07 GMT
WORKDIR /tmp
# Sun, 22 Mar 2026 18:31:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sun, 22 Mar 2026 18:31:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sun, 22 Mar 2026 18:31:27 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sun, 22 Mar 2026 18:31:27 GMT
ENTRYPOINT ["entrypoint"]
# Sun, 22 Mar 2026 18:31:27 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:90acba8ac92ad141ae919a99e64549b2f417e5b2ec79f1a99dbc8efba0fea96b`  
		Last Modified: Mon, 16 Mar 2026 22:09:11 GMT  
		Size: 47.8 MB (47792328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6add0609c3b541666acbd64d7040bade8e52829cb99e1fb5d81f0474186bee1e`  
		Last Modified: Sun, 22 Mar 2026 18:28:10 GMT  
		Size: 142.7 MB (142662936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a9c93f4e8bb065bcffd80f6b184be8912a632fc411d8b8cbb05f94a47333d7b`  
		Last Modified: Sun, 22 Mar 2026 18:35:53 GMT  
		Size: 84.5 MB (84459022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69f072ba7cfc17ae4e5ef896fae0daeb2e5c183e4729f70a9c962764ce05ce1`  
		Last Modified: Sun, 22 Mar 2026 18:35:40 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d6e5d38dc147f687452d263c92d9e317f90c54db964d8704df3724ffd8952c`  
		Last Modified: Sun, 22 Mar 2026 18:35:40 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d9e3ceb7215b526ab15595dc7fba34f7056072cca3a19c2a9d717e74c742bc02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7472465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d2309d99270742ea389ea4c82c30b37a20e29dd79d6d31ec8a21fccea7a6543`

```dockerfile
```

-	Layers:
	-	`sha256:f068f99564984a0aca677370c89e804dca1d46035e8347d7d21e0a3bd92a208f`  
		Last Modified: Sun, 22 Mar 2026 18:35:42 GMT  
		Size: 7.5 MB (7456663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f517eb3dccc51a3ec0196e28bc8f499d8860e34ac8f54594d9dcb59861857c9`  
		Last Modified: Sun, 22 Mar 2026 18:35:39 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:f08f1e7f6961a3d36c78353491dfab3500f90988aec0a125faa8dddc093d527e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.5 MB (271537398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e0f4a01498f87338919c6429f9cb8782a410b3476bd6fd297a4caa2f0164cd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 11:38:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 11:38:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 11:38:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 11:38:14 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 11:38:14 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 11:38:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 11:38:49 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 11:38:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 11:38:49 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 11:38:49 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7bc76783a6155f9347e92234e4b5c38bd02638c6de782f4623d0736c769250f0`  
		Last Modified: Mon, 16 Mar 2026 21:52:57 GMT  
		Size: 49.4 MB (49364775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0e873883d06c3d66937d1b59b9c75c3451b6c0508819963b4679d67d56b74c`  
		Last Modified: Tue, 17 Mar 2026 11:39:29 GMT  
		Size: 135.6 MB (135626794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dce659ad6837cfd9848b82516620de7a17b108d78fe5d71af59ff45354e5c47`  
		Last Modified: Tue, 17 Mar 2026 11:39:30 GMT  
		Size: 86.5 MB (86544786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc002232db3caef7cd659f3fe252614c9e3a5e36e397ccf750585dc0ec2e233`  
		Last Modified: Tue, 17 Mar 2026 11:39:28 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526b39e47290645406fdeffe5e9d97c15fe22f0cdb2b7a006a3a4ebdffc90290`  
		Last Modified: Tue, 17 Mar 2026 11:39:28 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:ebfff3dba69fbd4d7fb95b91b2f5a04bec022353009e76a2e923825589f29240
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7482343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2e6409197409b7313ebd627012a931fde9c375d85bd5a5b4da6fedfc39e0f28`

```dockerfile
```

-	Layers:
	-	`sha256:99407ea26d8c5fcb25d38e1c1418fbfe85dce72a15d001cfcb61c444ada3ebfa`  
		Last Modified: Tue, 17 Mar 2026 11:39:29 GMT  
		Size: 7.5 MB (7466589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0dead34be928309ca50553e17468adafaa452df070981c625c55aee613b19abf`  
		Last Modified: Tue, 17 Mar 2026 11:39:28 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json
