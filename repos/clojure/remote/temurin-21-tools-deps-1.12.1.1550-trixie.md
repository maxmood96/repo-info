## `clojure:temurin-21-tools-deps-1.12.1.1550-trixie`

```console
$ docker pull clojure@sha256:a9d3a402f8981906c4db1569f0361aae6ccb3c222af30273a89202df92a07170
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

### `clojure:temurin-21-tools-deps-1.12.1.1550-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:22ce9653c6600b0f1a3e72c1f8ce574901253ec47b22ea3c2fceab2548cbd8f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292469955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11aae1d8ed18db771e5da8f1fafb5d5f4c052a12598785004103c74bddb102a5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
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
	-	`sha256:80b7316254b3093eb3c7ac44bb6c34bde013f27947c1ed8d8afe456b957ebfdb`  
		Last Modified: Tue, 12 Aug 2025 20:45:14 GMT  
		Size: 49.3 MB (49278280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11046dbd54d04576b031644288b0b1a232e139b9c61c50238d2f40d4eb0f2cc3`  
		Last Modified: Wed, 13 Aug 2025 04:24:17 GMT  
		Size: 157.8 MB (157804748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df9833b4e2728e8893b716029522c7b45387a52e1098cc3024ab21b3d1d6c7f`  
		Last Modified: Tue, 12 Aug 2025 21:38:02 GMT  
		Size: 85.4 MB (85385887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ffd3ea412acc552dbddf0b0ca2b2f6d8d51cdc71d89c14aabadc8f8e967b1dc`  
		Last Modified: Tue, 12 Aug 2025 21:37:49 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4abd7782be9461577e5246884acdc49e5c35da8b0fe8b38ebdb377f6bbccb013`  
		Last Modified: Tue, 12 Aug 2025 21:37:50 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.1.1550-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a710729eab708fb43155c2b4b3cfc79705d8362136e3008ae8abb20511f9b6c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7482427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e289293c4e86e98353c67f246640f30874866ec1e7392df004ddba8be7c6ac0e`

```dockerfile
```

-	Layers:
	-	`sha256:e7b3387724fe19b22b1eee42ff05485748b1d5455bbc5b5a1d95a2d289bfee40`  
		Last Modified: Wed, 13 Aug 2025 00:39:20 GMT  
		Size: 7.5 MB (7465962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db35645532e3a7b751334a4fbd23ee09ff6e1bae9db336473924399230fe5320`  
		Last Modified: Wed, 13 Aug 2025 00:39:21 GMT  
		Size: 16.5 KB (16465 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.1.1550-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:053c52a7271bb25016e1017de9a4d5da2e930757505506b166cfd9839c3d74a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.9 MB (290935117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e57cc3a82a7e01bf7f5c09efed56bcd4706402ca17fba4647f2f458afbd654f5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
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
	-	`sha256:d1e40442030765a3ac5d135c39154d052eba20953ea0e5d35a066f7722cdd93d`  
		Last Modified: Tue, 12 Aug 2025 22:12:36 GMT  
		Size: 49.6 MB (49641603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2270db57ed7921cee5a118a272c4250c32db773ac67ed678674ac19ad0a5050d`  
		Last Modified: Thu, 14 Aug 2025 07:23:06 GMT  
		Size: 156.1 MB (156081225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a51f60699faf958f0709027239bb72932f9632fe86b526ed8d6260c11795869`  
		Last Modified: Wed, 13 Aug 2025 14:39:11 GMT  
		Size: 85.2 MB (85211247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04580630866a0cc572de9e16f2bf136d1cba49b4ca27ede325ff23e77880968d`  
		Last Modified: Wed, 13 Aug 2025 14:38:52 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10434f9fa38ccb3359a0fe5252f64381d67ea84d6f2be59d3da99b6c9c07140c`  
		Last Modified: Wed, 13 Aug 2025 14:38:52 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.1.1550-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:1575057114423f2be2e784ab94abafd16b408093d096cfb1b30a2a334a7351d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7489623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee8a600bbe14046f243d0bc237c129b45a0d54a9ef6ea8d77a279c2fe93ef2b6`

```dockerfile
```

-	Layers:
	-	`sha256:80ebbc2de7e94863ad28ea51d228ba018fc7393bf91a8f29487ec1be8297bc71`  
		Last Modified: Wed, 13 Aug 2025 15:39:52 GMT  
		Size: 7.5 MB (7473016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da5daba50a699c089f3280caa2e30b625869702502c311fd275f443b900fbe13`  
		Last Modified: Wed, 13 Aug 2025 15:39:53 GMT  
		Size: 16.6 KB (16607 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.1.1550-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:bd95a27ef550d129fb57b55f28f7b09f2995c14bd6c4b0d41f3daf19f2934bca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.9 MB (301863047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e36b9cfd29b16be93a7b4d694cd195c0cf617391a426801c85f49c91011303b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
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
	-	`sha256:befe77620590f63939f5bcadadc9f45832981822c9c901f057eb4e86f733c29a`  
		Last Modified: Wed, 13 Aug 2025 00:32:04 GMT  
		Size: 53.1 MB (53103384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21fc32363139243e018fa10b3548cea5d08ae8b6641c47a615b4649b945d62f7`  
		Last Modified: Wed, 13 Aug 2025 20:06:04 GMT  
		Size: 158.0 MB (157963438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08cd26cce561172a5d82210291dba63a1d1b4cb1a09fbe67a5b0520834e03ce2`  
		Last Modified: Wed, 13 Aug 2025 20:14:02 GMT  
		Size: 90.8 MB (90795183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:489d11047d89ca1b93dfd8fd913458010e8fb06200feb18b80bb6913968d4773`  
		Last Modified: Wed, 13 Aug 2025 20:13:58 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a7859045500f969f464da942996e19950994cfcabb86c10cfca2230de701114`  
		Last Modified: Wed, 13 Aug 2025 20:13:59 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.1.1550-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:1e62a87712b0259249de088530ebc7d38f6132a186cae558a03de437e0617a5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7486918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f62dcf291b14eb5712f8898e2389a6da83914a04ca5051aa321008292694987`

```dockerfile
```

-	Layers:
	-	`sha256:3541b3474e0ec4327bbb024e39026995ac9f82c9502760ec4edf7c799c00be7f`  
		Last Modified: Wed, 13 Aug 2025 21:38:38 GMT  
		Size: 7.5 MB (7470393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0d3bd981a27e45797fe4e3a54fcb348d2910aafb11365a11ef981e630ee1769`  
		Last Modified: Wed, 13 Aug 2025 21:38:39 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.1.1550-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:c94e73b350d3de4f0c8a3d5e3381ad4254d747b8a212ca338ab2dad989cdc416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.6 MB (285634963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad66acee69bef5a67c2e8c1483d28a09b99e24f44fadc6fe33b73439247104fd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
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
	-	`sha256:59f3e0adb655cb03f7d489f3cc57e302e249916bbb076c78008f9329238bfb20`  
		Last Modified: Wed, 13 Aug 2025 01:13:55 GMT  
		Size: 47.8 MB (47764303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ae40206fce815f54e732cda12724589c8a4bd14b341d3c3b2cb34415f3acc91`  
		Last Modified: Fri, 15 Aug 2025 17:55:13 GMT  
		Size: 153.6 MB (153593531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d62820487fc5d1391fd18eee41e34e85cb1bb2dbc09acfc36adcb18ee5dcb0ba`  
		Last Modified: Fri, 15 Aug 2025 07:52:11 GMT  
		Size: 84.3 MB (84276086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b339df3d1823d3f201b9850f3d8fdc24cfb67251cde0256ce1898de418d96d`  
		Last Modified: Fri, 15 Aug 2025 07:52:01 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b1926b6c980b7203093de8bcd01eeac4e73e5daff590421fc1e744e38f6126`  
		Last Modified: Fri, 15 Aug 2025 07:52:01 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.1.1550-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:0a509f5e3505f209ee933fff395137b555cb7336fc83e431953ca4d8e9810c9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7470411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e331b1f97121eebfc0a57c9dd142c317bed0aa7a2e32430788b2e7c4d8476eea`

```dockerfile
```

-	Layers:
	-	`sha256:bf501ad99ae8939c4adbf3e26ef56f10922f062fcdbe75bd011e63d8b94298bf`  
		Last Modified: Fri, 15 Aug 2025 09:36:55 GMT  
		Size: 7.5 MB (7453887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1ce2d88696b25776e0ea6a5b13366c27753709489fe893385ecd89bda17ba50`  
		Last Modified: Fri, 15 Aug 2025 09:36:56 GMT  
		Size: 16.5 KB (16524 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.1.1550-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:faef2ca4c678367f586be285ca2ba7c3632cedb6bb0ad8f0ca87c237290e43b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.7 MB (282726947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:647dadfd91906935c84abfffc96028e8db894a8b992916de172453ca3b49be0a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
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
	-	`sha256:c3b791adea90b39bc59919a9959b7f44f65aa3364a03dd0271a5ff658488877f`  
		Last Modified: Tue, 12 Aug 2025 20:59:03 GMT  
		Size: 49.3 MB (49345161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd61649b861403cbb63fef0cd938368dd06eb20d55b31215384266d7d8d3068`  
		Last Modified: Wed, 13 Aug 2025 07:20:43 GMT  
		Size: 147.0 MB (147026960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9afd72ed605768bcb88ca0a18a9937c481866f16ab2f6e30b467efb08810a2`  
		Last Modified: Wed, 13 Aug 2025 07:24:02 GMT  
		Size: 86.4 MB (86353782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc5ca555d89c1308330e75bb731d509a2aad3e8322e9fe81e9680726a5a5a26`  
		Last Modified: Wed, 13 Aug 2025 07:24:30 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2dc9486b22f42fe0632f9961d5394e142bd276bb095a7abb865819ef1ce920`  
		Last Modified: Wed, 13 Aug 2025 07:24:30 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.1.1550-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:57f6596b11cf9b390801b668909358f576cac1359773ef4d2ef7da4cf2e8f532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7478349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92fc55d376ad9c2299f64bc57d905500cbc01415d8ec5855a583c60f85d8b6c5`

```dockerfile
```

-	Layers:
	-	`sha256:dfceb56ba90c8a05251c068d1e904f2f438f61e1fa1658da032f0c0792018aa4`  
		Last Modified: Wed, 13 Aug 2025 09:38:03 GMT  
		Size: 7.5 MB (7461884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:448d16bf2d6ff5012b6db7eecc31efd13fa9118a841195c519c367043eb885e1`  
		Last Modified: Wed, 13 Aug 2025 09:38:03 GMT  
		Size: 16.5 KB (16465 bytes)  
		MIME: application/vnd.in-toto+json
