## `clojure:temurin-25-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:b19d8ac2c0369caef8e37d85549f7437fd5164978157c6638229e26df5324cad
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

### `clojure:temurin-25-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f69560ad796b977b4254fdf4a79e4ab62cea660521ac106d98063fe06ec0593d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.2 MB (190192799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f04036fa3998752285e97c6e5e4e7c4b1860205601972f51e28c08be10ad5bbd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Wed, 15 Apr 2026 22:06:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:06:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:06:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:06:43 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:06:43 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:06:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:06:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:06:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:06:57 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:06:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e37cc7d902a86c38ce1e23e9c33f70d245f7c5e842c46b908b301874ed87b19`  
		Last Modified: Wed, 15 Apr 2026 22:07:19 GMT  
		Size: 92.3 MB (92256337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd36792dc864c950aa7fe81fa0d52135b2c7944982fe1d86a1da8eea5b836dbd`  
		Last Modified: Wed, 15 Apr 2026 22:07:18 GMT  
		Size: 69.7 MB (69699086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4279beb899d705995252e6273169d9fab87da7daa02982b0c095f3abe3f6c6cb`  
		Last Modified: Wed, 15 Apr 2026 22:07:15 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b519771eb9288b37717cf8109b28ecb63ea7b014fe4674c69cd5edbac1b9707`  
		Last Modified: Wed, 15 Apr 2026 22:07:15 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fa4d7b95a1126815b05695b4139c75bfa7c8ce916660b5365f25d8c8426f6fd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5100786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eec65e4898a9161abdbaceb511e4188b7eb25b87d494a79b53e2585b5cbe6a76`

```dockerfile
```

-	Layers:
	-	`sha256:ccc4ee1ee94b74b26db80b57d4c038fcd4ee00b14c9f4db259d0809d39f1ac8f`  
		Last Modified: Wed, 15 Apr 2026 22:07:15 GMT  
		Size: 5.1 MB (5084261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1df2f298726d5430aa770886fb8ff3686139327ba58a2444951015f747940aa`  
		Last Modified: Wed, 15 Apr 2026 22:07:14 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:924cb9539990cba155760bf9f861d85fb0f0ba264ef7d903d226ea9feb4a3994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.1 MB (189096558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e162f11d726bf1eb14fcaea2b574ed313fdc97818a81b0f623bad0a4f6d9ed2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Wed, 15 Apr 2026 22:18:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:18:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:18:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:18:17 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:18:17 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:18:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:18:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:18:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:18:32 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:18:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f94dc77f38f4c056130c872d76c2a44360df6ee9c4f106b284a49aacd986918a`  
		Last Modified: Wed, 15 Apr 2026 22:18:53 GMT  
		Size: 91.3 MB (91288271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aba6700d4049da5089d33efa60d27ca3f3640672a75c79a6d1a5a3e722bc5bc`  
		Last Modified: Wed, 15 Apr 2026 22:18:53 GMT  
		Size: 69.7 MB (69691082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986c9d436f0af92663da4898f483785bde5f09bed6f180c211f3e11c59a7d22c`  
		Last Modified: Wed, 15 Apr 2026 22:18:49 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b59c285d038a671b991d2f24e44e0e09706eebbcfe9ec333cc9c01cd1bb5022`  
		Last Modified: Wed, 15 Apr 2026 22:18:49 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:086cff321b60186fa301ecd976a331941fea04f6554a8445e3e9debfd169790c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5106710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c32c01b63146833f109baab077222a1f6f27b6f5ad5e243ded5accf2050bb1b8`

```dockerfile
```

-	Layers:
	-	`sha256:e8322096970c2f97bb3d315b8159fdbf551df93feaef15aa0a0097ddf4c3d7df`  
		Last Modified: Wed, 15 Apr 2026 22:18:49 GMT  
		Size: 5.1 MB (5090043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fca8511a00bc92397bcdff7561dc85a84346fb89f50bc5e34c1076756b0a03ae`  
		Last Modified: Wed, 15 Apr 2026 22:18:49 GMT  
		Size: 16.7 KB (16667 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:651c95a7f5b208f47173f6b9c9fde0358af70649233f44b226d0faa4258661ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.2 MB (199242786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8c75b337764760e46cade9d4a4a6f05a42c3b155c0418b0efe515b7b8f021aa`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 19:13:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 19:13:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 19:13:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 19:13:50 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 19:13:50 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 03:12:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 16 Apr 2026 03:12:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 16 Apr 2026 03:12:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 03:12:46 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 03:12:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b1c56220ca211bc9d02f1ed5c589465809676b6ab2cef705f1e2fb8e9726de76`  
		Last Modified: Tue, 07 Apr 2026 00:09:42 GMT  
		Size: 32.1 MB (32078464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:186825ad1954e238f9d41fa43dbe8881cdc35374805d5861befa0e42e394c10e`  
		Last Modified: Tue, 07 Apr 2026 19:15:05 GMT  
		Size: 91.6 MB (91632990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98e50018da8243a9b074e4f217112f41998683abe2200edb270fac370b50bdf`  
		Last Modified: Thu, 16 Apr 2026 03:13:18 GMT  
		Size: 75.5 MB (75530289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0301d95516079bc104e7fa7493070504907385432783624f3487eb2eb15354ab`  
		Last Modified: Thu, 16 Apr 2026 03:13:15 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5408b5dc137a9925c208a1339ac2e9b7326c02d29bcdf6f2cd08c58567e2d20e`  
		Last Modified: Thu, 16 Apr 2026 03:13:15 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8c955f108acf6fa285d665ce3285af69ffc5a76ef4ee7b3b6184b78e31c1e475
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5089328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3360bb0a285227d23c7100c9f51b5935413429f4145555bedd64aedb9d57fc9d`

```dockerfile
```

-	Layers:
	-	`sha256:511798b8f2ba6b8c4bcc2b16da39e1552559bb57c790b5cabb82566d09a34957`  
		Last Modified: Thu, 16 Apr 2026 03:13:16 GMT  
		Size: 5.1 MB (5072743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fffec5a02a1c01f9dc3f6d6504dcc2565d1f8593ecf37567e02f7457389a8b0`  
		Last Modified: Thu, 16 Apr 2026 03:13:15 GMT  
		Size: 16.6 KB (16585 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:6238e44cd4edac9cabb50d0291d84b84d726f76678bd9ceb9ca4cd3bb3b33b4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.6 MB (183639319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec9ca72211b4d9cf28bc44ecf5a4264b9c32c5ea5f4b75bd9c7aed06e79d85fb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Thu, 16 Apr 2026 00:43:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 00:43:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 00:43:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 00:43:49 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 16 Apr 2026 00:43:49 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 00:45:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 16 Apr 2026 00:45:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 16 Apr 2026 00:45:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 00:45:01 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 00:45:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c23087fbbda0d8352ee6b2d159c503459acb89da0eba1729b411ca394e68e292`  
		Last Modified: Tue, 07 Apr 2026 00:10:59 GMT  
		Size: 26.9 MB (26891634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a78ac609f8f046c6a31d61cf5e496d160fb1bf38a5cda92b8f538e5fc85bfd`  
		Last Modified: Thu, 16 Apr 2026 00:44:26 GMT  
		Size: 88.2 MB (88233823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0ec5c98363b0741c220393269c785f74da4bc8f4c8318d3a2879a2b0ca435b`  
		Last Modified: Thu, 16 Apr 2026 00:45:25 GMT  
		Size: 68.5 MB (68512818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:731a36ab7ac149be7871eb0b24f994b47dcc46a3e27698767808ceea9b4d9db3`  
		Last Modified: Thu, 16 Apr 2026 00:45:24 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65df5bda0c960ad8db49f2f61b65342578cf767a8142bd56c147a12b2a86a48e`  
		Last Modified: Thu, 16 Apr 2026 00:45:24 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2e2b4678e591636fafc6af5b0ca5f4cca5e2bf70925d96d65a00469a872ef924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5076667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c5dc25b633e6ad8104000600bc73be253250d270874138b5dfad00edd315534`

```dockerfile
```

-	Layers:
	-	`sha256:22da8d77210cf1f05a06521c4cdcaa48709c0129351a1568650114f0455eef20`  
		Last Modified: Thu, 16 Apr 2026 00:45:24 GMT  
		Size: 5.1 MB (5060144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38aadbb431004a05331fd83df6919530f0cc2969f01c8d09e7680b4a76f068eb`  
		Last Modified: Thu, 16 Apr 2026 00:45:24 GMT  
		Size: 16.5 KB (16523 bytes)  
		MIME: application/vnd.in-toto+json
