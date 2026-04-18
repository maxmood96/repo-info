## `clojure:temurin-25-tools-deps-trixie`

```console
$ docker pull clojure@sha256:2381ff6d23deb06e3916f43256bbb4c007aa6775ef0604e9e2f7002c710f4fc6
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

### `clojure:temurin-25-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:23b242c74308a4dd2f4b817e90d74df21f35dd16e1069d6e04d799b50cece7ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.6 MB (230635520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26d44041f84c7d744accf02211ed0dfbb0d2458149872014ca93afff060729e1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Wed, 15 Apr 2026 22:07:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:07:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:07:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:07:01 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:07:01 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:07:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:07:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:07:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:07:18 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:07:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a7730063fcfe708b222d34c4f07d633dfe087a28c05c4daaab2fa9943854c155`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 49.3 MB (49297833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5fecf4f5e7b670108e9e819d2dbc1d580bc84f1e670c002bb5590af738e268`  
		Last Modified: Wed, 15 Apr 2026 22:07:43 GMT  
		Size: 92.3 MB (92256335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8cdce79604453614516723ee10ca2d72c17c577710725ed796dfcb52cef651d`  
		Last Modified: Wed, 15 Apr 2026 22:07:44 GMT  
		Size: 89.1 MB (89080306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:112d5f6d0752ffa1581f63070ff20fc677a603cd29954318cdf48d130754fbc1`  
		Last Modified: Wed, 15 Apr 2026 22:07:39 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ade5603974c904bd0c8698d3435c048458e6071fe638f25bb07ad5a55700035d`  
		Last Modified: Wed, 15 Apr 2026 22:07:39 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:8de9b3fb6c47db13ebb75abf13bbe7d8bdbc1166ae20a59c72028e3f4d157a2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7455147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:528a95c9667708d3b381f72ebecaae7d30e37fbdb209133c02674d20820ee12b`

```dockerfile
```

-	Layers:
	-	`sha256:eb123c52fa9c5333c8f31cbdef978ab05d8c217af248b4cd95db286dedd35243`  
		Last Modified: Wed, 15 Apr 2026 22:07:40 GMT  
		Size: 7.4 MB (7438733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9fd859d68fe54317b959e3bfbd510639c5b6f73a765543a596d2a19c7551ba0`  
		Last Modified: Wed, 15 Apr 2026 22:07:39 GMT  
		Size: 16.4 KB (16414 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c59cf8ceb6b0f8aea0ab389b03ea5244cf46de8830be95b1f1f2137e755c5572
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.2 MB (230208028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1c46f1d1180692923e2ea09dec8f766b896513931e89b8c735d96d588cd6347`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Wed, 15 Apr 2026 22:18:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:18:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:18:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:18:38 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:18:38 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:18:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:18:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:18:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:18:57 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:18:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:912041a7b9f63b6550d3a3949c43e45f74a36a2f80c727e70e41cbe851de2d20`  
		Last Modified: Tue, 07 Apr 2026 00:11:19 GMT  
		Size: 49.7 MB (49665256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac33508e2a5cdcac0efc4fb7c48fc7735248007403be9fe795ef3917dbbf91c`  
		Last Modified: Wed, 15 Apr 2026 22:19:21 GMT  
		Size: 91.3 MB (91288275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7098e25e0f34860c49ee58f3bb4ab4bd237779e2f70d0b02f731582ef15c9554`  
		Last Modified: Wed, 15 Apr 2026 22:19:21 GMT  
		Size: 89.3 MB (89253454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd772916b7acef40182f6a42549b849a19d9918cad41dd4a594f8d5034a6c098`  
		Last Modified: Wed, 15 Apr 2026 22:19:17 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2763ba2feccdf1cbbd75216c67054dccaa3d7a8b7530eb4c2454d6c9c5047bb7`  
		Last Modified: Wed, 15 Apr 2026 22:19:17 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f34f7c509f54abbc495df418b36a032a92f84a9da729da143d837ea977010048
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7462340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a159e4f6c917715cdae1ab5bb5fba2e35d23e61026fdb6c8cb5be15a89379d4`

```dockerfile
```

-	Layers:
	-	`sha256:1d5a24c3c3154c78fdc754835930dc59ba498b159fb09c810a32248e7c0fb60f`  
		Last Modified: Wed, 15 Apr 2026 22:19:18 GMT  
		Size: 7.4 MB (7445784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb41078cb18e343de294b357cf96da757e7d37908b779eae02777056ad8aaf3b`  
		Last Modified: Wed, 15 Apr 2026 22:19:17 GMT  
		Size: 16.6 KB (16556 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:8b0b45b685a03f34708e706a24ec4a31b18fb6504748df3edaed23ea723d68f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.5 MB (239474473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f7150e0fc43c792f3e282de425d326e08407ded3adb1890d7c3f7e5ce2fdc4c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Thu, 16 Apr 2026 03:09:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 03:09:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 03:09:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 03:09:31 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 16 Apr 2026 03:09:32 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 03:14:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 16 Apr 2026 03:14:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 16 Apr 2026 03:14:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 03:14:14 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 03:14:14 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f2bea5beaa06af8495b6a91d35dc5ce3b11a84dad25d5c0a468a1e7008ed9e62`  
		Last Modified: Tue, 07 Apr 2026 00:12:52 GMT  
		Size: 53.1 MB (53118669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04092892db89c3f0f8309ba50439fcd1d5f508bb90c8bab723af681eadbd6ebd`  
		Last Modified: Thu, 16 Apr 2026 03:10:55 GMT  
		Size: 91.6 MB (91633017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc873e735bf0ddc5cec8afba5a7e0e2888512cc8b1c81a36954fa16d029dcdd`  
		Last Modified: Thu, 16 Apr 2026 03:14:52 GMT  
		Size: 94.7 MB (94721740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:996c6e20b38778dfebb53de739d0b07dfb8553695a88d42aa1914fa3f0cf67ef`  
		Last Modified: Thu, 16 Apr 2026 03:14:49 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d069ce35a37f8d826145a0546423a93176b2999a633fd6cd5b8d7f329145200`  
		Last Modified: Thu, 16 Apr 2026 03:14:49 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b9ccf321760efe1e287066adfe38e5df96918a46085ccebc8788a5d17f4333af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7442953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b7525a8c23d94e36bf053ad974dd54ce1e7ca39fadd0426e1022b51427ba11`

```dockerfile
```

-	Layers:
	-	`sha256:df408ea668da0ab193fe2b0da6e5715a1a28a2eda15ed1b718dda4bca5dab2f1`  
		Last Modified: Thu, 16 Apr 2026 03:14:50 GMT  
		Size: 7.4 MB (7426478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:314f093d962bbd912da1b1385c024d50deae4faf57fb7a5d78b81a6d803ca296`  
		Last Modified: Thu, 16 Apr 2026 03:14:49 GMT  
		Size: 16.5 KB (16475 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:70bd8c713be80e60b2e7415b27d306935d44f53a22edd2794d9961fb137e7b0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.2 MB (226198211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57d4e1d90beb11e81b476ea7ca4fbbdc29f30753810edd90cf2886ae9e0e1cf9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Sat, 11 Apr 2026 22:33:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 11 Apr 2026 22:33:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 11 Apr 2026 22:33:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 11 Apr 2026 22:33:17 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Sat, 18 Apr 2026 05:20:11 GMT
WORKDIR /tmp
# Sat, 18 Apr 2026 05:38:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 18 Apr 2026 05:38:02 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 18 Apr 2026 05:38:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 18 Apr 2026 05:38:02 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 18 Apr 2026 05:38:02 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3e61abfb88ee12dd42b3c32c20825f42c0eae3286fe2a9301e326413688c3d40`  
		Last Modified: Tue, 07 Apr 2026 01:54:08 GMT  
		Size: 47.8 MB (47792626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7224fd307fae2068f62ccce22d637a96c5204dea7af1d7b9116b5323460f86`  
		Last Modified: Sat, 11 Apr 2026 22:38:56 GMT  
		Size: 90.8 MB (90773425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a36285e3dcd25f7a44c612fe778c8bfa02539ab933cb5dfab0d73cad6bde9f99`  
		Last Modified: Sat, 18 Apr 2026 05:42:25 GMT  
		Size: 87.6 MB (87631116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fae0c36a735ece9d0072456cd03f8456e3c4edc9b276ff8caefc6d44b19061c`  
		Last Modified: Sat, 18 Apr 2026 05:42:11 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b4e6da25fabe255b73f61f64e62349291cb6a8778d7372ebe8aee9c4665d5ac`  
		Last Modified: Sat, 18 Apr 2026 05:42:11 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e916eb5531ec1a92cb6a48dd4c168c4b2f24b4df5cc28cc4cd3b7c1ae1156ae7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7425146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86d39c73f4cb1fd1c9ccbd030db0b0faedbde0ae178f1585e0a3ba12069c65cf`

```dockerfile
```

-	Layers:
	-	`sha256:6902f2ccfc03419e376164de517c37b1e9f831dc543d60c50a41c360db7d740c`  
		Last Modified: Sat, 18 Apr 2026 05:42:13 GMT  
		Size: 7.4 MB (7408671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:302f1b2422efca550412701c9a5c4c52bce4d0c1fc9fa860054a0d4704d49433`  
		Last Modified: Sat, 18 Apr 2026 05:42:10 GMT  
		Size: 16.5 KB (16475 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:bf919c43c84eafe52458b275a9a0804228418cd137be755cacfc3274b798aa6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.3 MB (227310524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7a2ab9daba956d36848778e859688658582472f60ab445e3c54c25ed68592c9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Thu, 16 Apr 2026 00:44:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 00:44:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 00:44:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 00:44:04 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 16 Apr 2026 00:44:04 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 00:45:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 16 Apr 2026 00:45:47 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 16 Apr 2026 00:45:47 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 00:45:47 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 00:45:47 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:99ccdb9e0b0ce79a36cbcc433fd972b049c1e4e84d217954de0e89224b1fb094`  
		Last Modified: Tue, 07 Apr 2026 00:13:49 GMT  
		Size: 49.4 MB (49365104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af85e16ff2a5e4ef4e7bca442eaf789074eba5dae2548a5309ae1cc069f92daf`  
		Last Modified: Thu, 16 Apr 2026 00:44:45 GMT  
		Size: 88.2 MB (88233823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11d3893f14bdd8b7e4b96dfe283c4d22679a85c5136d4b7dfa76cb2d664cc5bb`  
		Last Modified: Thu, 16 Apr 2026 00:46:15 GMT  
		Size: 89.7 MB (89710555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92891227399ad31b4c349aa68167619a71b8c6613f6d3be4fb1aa5b5b9303da`  
		Last Modified: Thu, 16 Apr 2026 00:46:12 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59ab526f9c54f993a94974b92e4cbd230af6ee06d615b26a436fd509be3c850`  
		Last Modified: Thu, 16 Apr 2026 00:46:11 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:206c679d1e1994c9b59d2d194f13a6bebe2ca1a776e35efa61b60b83d7fb0f33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7435632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9114e6049e36f0b6c29f07421d3e5440d8f0f16e9e544ee1a694e72750d5568f`

```dockerfile
```

-	Layers:
	-	`sha256:8c231f8c72e11ee968ee378552c874b84b5a09f79b79431e6040b2f64deb1e82`  
		Last Modified: Thu, 16 Apr 2026 00:46:12 GMT  
		Size: 7.4 MB (7419217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a8be6f657c97c12e06431390d79c2b793a86ca6ce7a8826dba70e3af4efb7f0`  
		Last Modified: Thu, 16 Apr 2026 00:46:11 GMT  
		Size: 16.4 KB (16415 bytes)  
		MIME: application/vnd.in-toto+json
