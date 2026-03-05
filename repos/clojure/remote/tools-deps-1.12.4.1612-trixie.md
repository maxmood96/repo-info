## `clojure:tools-deps-1.12.4.1612-trixie`

```console
$ docker pull clojure@sha256:130e743bd2959a5107c50ba702930f7eaf3abd1033d6a2648457d3a3718b974b
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

### `clojure:tools-deps-1.12.4.1612-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:ff265f6c5cfb9f70606050fde8b5027e0606cb929377281a747a3463f69bba19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.1 MB (227117550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e384929a7bab8155ab7636ae62481266e07c0890ed8b2320a35133de15154d41`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Wed, 04 Mar 2026 17:51:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:51:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:51:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:51:40 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:51:40 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:51:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:51:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:51:56 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 04 Mar 2026 17:51:56 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Mar 2026 17:51:56 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:866771c43bf5eb77362eeeb163c0c825e194c2806d0b697028434e3b9c02f59d`  
		Last Modified: Tue, 24 Feb 2026 18:43:22 GMT  
		Size: 49.3 MB (49293124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a29b946c327f2d4dec13feccfd1e9a03cdeaa6002e9a72694f1cf5e4a694b7`  
		Last Modified: Wed, 04 Mar 2026 17:52:17 GMT  
		Size: 92.3 MB (92256315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a25bc91d69dd3b57af8acf8c34ff47682d242fea0b3057b229420d620fefafa`  
		Last Modified: Wed, 04 Mar 2026 17:52:17 GMT  
		Size: 85.6 MB (85567069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6a17a5daaf29abb44f8fb3afff2377c6d294857c555ac8ee1a1e251853ed20`  
		Last Modified: Wed, 04 Mar 2026 17:52:13 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1dfdd63448559d86fe859c67250052a92ea5d73887104ea6d5564fa48822b7f`  
		Last Modified: Wed, 04 Mar 2026 17:52:14 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1612-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:cc8ac48d5370b118161add6e6aa2f07257902c4729ef8e2bae7a59f4002832f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7455074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c9cdd76dcae49b00d7528f7c4d1685dd3fe692704ee5dd770a73a2f2182d54c`

```dockerfile
```

-	Layers:
	-	`sha256:ee7d6a428c573bdbee0f59af781c4213660dd67d2480935aaba0eb90f805a508`  
		Last Modified: Wed, 04 Mar 2026 17:52:14 GMT  
		Size: 7.4 MB (7438659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af7920fd5dc8b96989965f832acc73e6572ba7785d78c88700a5d33765d20af8`  
		Last Modified: Wed, 04 Mar 2026 17:52:13 GMT  
		Size: 16.4 KB (16415 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1612-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:efa55e644a73062cc9f67fdbf6c1c3ae33c0bde730ff624ef02e42fccdd65dff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226324309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d352f13f31f4aa7a20fbd183b6c7d6acd456bc368c07f1b360d0377ca662251`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Wed, 04 Mar 2026 17:51:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:51:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:51:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:51:20 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:51:20 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:51:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:51:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:51:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 04 Mar 2026 17:51:39 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Mar 2026 17:51:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ac9148dc57ca750b09f3f3da6f16324e1a3b62432b2726734535ec610e1a9232`  
		Last Modified: Tue, 24 Feb 2026 18:42:56 GMT  
		Size: 49.7 MB (49652168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152fc7a2905a3cce8fd8b9b6f36ab28ee98528c9154718d1933727d046f09a8c`  
		Last Modified: Wed, 04 Mar 2026 17:52:02 GMT  
		Size: 91.3 MB (91288289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5317b2019fe919a760b90f1be0477e76b7280460c1c6e724b0a9c8bb5b4597c`  
		Last Modified: Wed, 04 Mar 2026 17:52:02 GMT  
		Size: 85.4 MB (85382812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57bd9cda67029221ab54738445d8dbf20a595c20a3abcca3767c4dfa1f0d97d`  
		Last Modified: Wed, 04 Mar 2026 17:51:59 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa88b8307c3d9a6d3d9458f1e6417a647a275a9d4b171747bbdd949aa618de8`  
		Last Modified: Wed, 04 Mar 2026 17:51:59 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1612-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:1f3ecdb6b97c1f53436646ef9778c500bfdacf83a31cc274dd87cf454f7d22fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7462267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fb6243d9aa0546aa1c786c6e6ad3bf24987a8f6877cbf4146e7ae375eeda828`

```dockerfile
```

-	Layers:
	-	`sha256:b4f1d1f77f660b3d92963f8544e0fc06d24c8ac4164e4e5bfe48cfe5a98bb71e`  
		Last Modified: Wed, 04 Mar 2026 17:51:59 GMT  
		Size: 7.4 MB (7445710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37e382c236df9ebb0546276aaa894c191d8549b8936e419d06c100adae8f4b9d`  
		Last Modified: Wed, 04 Mar 2026 17:51:59 GMT  
		Size: 16.6 KB (16557 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1612-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:d0cddb4d2d3b9d065d3ce96aa7ad14d541082e6a139a17902727e7b45d3805f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.7 MB (235722960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:160236b3b27fca31235039b64d345c23d00cea1be9bcb47a0ecd539b5c4ea008`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Wed, 04 Mar 2026 18:10:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 18:10:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 18:10:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 18:10:33 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 18:10:34 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 18:11:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 18:11:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 18:11:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 04 Mar 2026 18:11:34 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Mar 2026 18:11:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:468eb7cd0e9ceb9e5b1c4c9daadd36c2fd1f1ee82c667dc1a7d70fa95600a20f`  
		Last Modified: Tue, 24 Feb 2026 18:45:11 GMT  
		Size: 53.1 MB (53112261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ed0558160b3e06346322bebf948770c5aee048d8fa085104adf72c3c99550f`  
		Last Modified: Wed, 04 Mar 2026 18:12:20 GMT  
		Size: 91.6 MB (91632955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def3e246af8f927b881508c1ddb9246178b3f6a9e14f8457079663063cbb4d3f`  
		Last Modified: Wed, 04 Mar 2026 18:12:21 GMT  
		Size: 91.0 MB (90976701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34881fe1602ffa8463f87c2554b6424d8299d7ed573c8535f197fac83ce0c2d0`  
		Last Modified: Wed, 04 Mar 2026 18:12:16 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1c265b0239b701e3932784004e9b7f5480fd2eb8bc527ec2526010df57e039`  
		Last Modified: Wed, 04 Mar 2026 18:12:17 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1612-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:743e6e5b79333bbbd3476ba72a9d4ab8e8d0080c99987400edb6c4ac21c3b898
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7442879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aef18e875585c5b69e60c64cd2508b1f7c0e98f211226bfba3ebc40eef7ca71`

```dockerfile
```

-	Layers:
	-	`sha256:e4f52224e9f218b885ddd58c0d91032910f4816e87b7d403551d9276ce8caf10`  
		Last Modified: Wed, 04 Mar 2026 18:12:17 GMT  
		Size: 7.4 MB (7426404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e99709e645a7605a957f0dec99676c2fa43b64537c5f0b2340bffa722a63151`  
		Last Modified: Wed, 04 Mar 2026 18:12:16 GMT  
		Size: 16.5 KB (16475 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1612-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:c81fedf91b7c6ac6b5919d21bc5281626aeff8199b841db57eae5434e7ef8ac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.0 MB (223003928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9c33a712b9de99d24da0f7cc8a87762c5b41ee8d2a1cc4c81ab96456d6b02de`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Wed, 04 Mar 2026 11:38:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 11:38:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 11:38:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 11:38:19 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 11:38:19 GMT
WORKDIR /tmp
# Thu, 05 Mar 2026 06:58:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Mar 2026 06:58:21 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Mar 2026 06:58:21 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Mar 2026 06:58:21 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Mar 2026 06:58:21 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3be247472b67578a1d05739722d8adeca41098796e5d6210800176db58046fa7`  
		Last Modified: Tue, 24 Feb 2026 18:57:42 GMT  
		Size: 47.8 MB (47776936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8c80deefa5794092a24432da9b0e8a50fb59fc32467cb68891a413c01800f5`  
		Last Modified: Wed, 04 Mar 2026 11:45:55 GMT  
		Size: 90.8 MB (90773397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51786f57f5f5b0e042439d204dcf7af649a7d43037d3b9bccfc8083d72b2087d`  
		Last Modified: Thu, 05 Mar 2026 07:02:37 GMT  
		Size: 84.5 MB (84452550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93eb8b817bb97d0f8ae912e206ce312009483bfca841aa6cb8c2ee0fad152ea6`  
		Last Modified: Thu, 05 Mar 2026 07:02:24 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cce4fce6581dcac2647ab6544d81912fd1a045b9106c8069c9a6e4c1d036acc4`  
		Last Modified: Thu, 05 Mar 2026 07:02:24 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1612-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:bd6f5c758c1cb18d49abff0ab569cefbe181ac078d215d22e1b973d240dca238
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7425072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87d9b486f9c40643297845115ef2357ababe8d3550887a5f2948c92a2ab840d9`

```dockerfile
```

-	Layers:
	-	`sha256:c7849ac1ac4eb9b5a628114a873e597f8ce2bdbbd316f5365eacc9b17d20178c`  
		Last Modified: Thu, 05 Mar 2026 07:02:26 GMT  
		Size: 7.4 MB (7408597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1bf592a4bfb6545c2074d9f8138af4570cf4bb3c29cb1dc4e1552195163f10c`  
		Last Modified: Thu, 05 Mar 2026 07:02:23 GMT  
		Size: 16.5 KB (16475 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1612-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:d23722a8409785c4beeb49130b4dc3aa8b6eb0d4e99f02c7aef4af1e2e957684
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.1 MB (224119023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f1b01a4c9e5e45a27587e40718217bfe324dc0db056532a4b77635103e4262d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Wed, 04 Mar 2026 17:52:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:52:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:52:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:52:30 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:52:30 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:52:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:52:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:52:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 04 Mar 2026 17:52:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Mar 2026 17:52:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:aba9aa950add2749194487d5c63a3069af6daf9dfe54d80cfbe32bfa7a5faa07`  
		Last Modified: Tue, 24 Feb 2026 18:43:53 GMT  
		Size: 49.4 MB (49354534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ca30e38dbf8caa5f67ae6bee40c66c4a29c708a7abf40f68030fd409b940e95`  
		Last Modified: Wed, 04 Mar 2026 17:53:15 GMT  
		Size: 88.2 MB (88233824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c758a0549f800bc78f8c471800ca7fc4b33259d53f30986cf0ed450c23cc53`  
		Last Modified: Wed, 04 Mar 2026 17:53:15 GMT  
		Size: 86.5 MB (86529623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e586c3818950998f1b13f2e5186fc5a313d94e779953fdbf35c1691a50c4a4ef`  
		Last Modified: Wed, 04 Mar 2026 17:53:13 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d6285166a44bbf10b58945120fe408401fae8d5c5d153f5f92e463de7165f7`  
		Last Modified: Wed, 04 Mar 2026 17:53:13 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1612-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:19594fa678d3ef404d9279746b0a2e14d8c21198c9d77007530e98a324e6e6d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7435558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:720791c0913cd6618652aa6f3521d7c63e93a16f328a1210160a0bd4c2dc0655`

```dockerfile
```

-	Layers:
	-	`sha256:529ddc98eb636ab38d57e0567077f0a8c84959bfa9568545e69ca447a97afe5b`  
		Last Modified: Wed, 04 Mar 2026 17:53:13 GMT  
		Size: 7.4 MB (7419143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63b002aa371dbd3cc8c8d45160efaf29c3c9391dbfc468dd6cdf931709da8617`  
		Last Modified: Wed, 04 Mar 2026 17:53:13 GMT  
		Size: 16.4 KB (16415 bytes)  
		MIME: application/vnd.in-toto+json
