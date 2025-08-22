## `clojure:temurin-24-tools-deps-1.12.1.1561-trixie`

```console
$ docker pull clojure@sha256:bbeae8fcaa4b61d8d0aff073bc73c90fca55e04af0c9e52e69abdfd7eee577f8
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

### `clojure:temurin-24-tools-deps-1.12.1.1561-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:1947c140e4b6cee94f31cd189ac1934960c1b778a5503cc02f2d0dc24afc4e6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.7 MB (224690881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce6ce7cc29d030168a73a4eeb976148464d7c56184dda4c4cd55efd2e7bd6cea`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:80b7316254b3093eb3c7ac44bb6c34bde013f27947c1ed8d8afe456b957ebfdb`  
		Last Modified: Tue, 12 Aug 2025 20:45:14 GMT  
		Size: 49.3 MB (49278280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db281ae0e62a1d4470d3c0130cf5673f0c1ea6d2d5621196455ab6347630470a`  
		Last Modified: Mon, 18 Aug 2025 16:53:25 GMT  
		Size: 90.0 MB (89975262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca2b28b0b278cc356e7c1346a6da5866b567e336438396e27a60b2d200b3769`  
		Last Modified: Mon, 18 Aug 2025 16:53:26 GMT  
		Size: 85.4 MB (85436297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76fab68211c415467aadff4ce875bfbfc7b169961a21cdbb3852a2f8640de4c4`  
		Last Modified: Mon, 18 Aug 2025 16:53:14 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:384fe58b76589a8e5f1b3c15c2ec0ead08f0d956543fda80cbc16fc4b06d1f7f`  
		Last Modified: Mon, 18 Aug 2025 16:53:14 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1561-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:57e735d6bbaaadfa33e5df467c5418f1dee83a7a7bd19477893093fdc20b6422
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7428659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5176403f0c0577e1820afc9a08408b609e4e9d5edef5e813fb91ac5e8d4648c5`

```dockerfile
```

-	Layers:
	-	`sha256:239bb153207bb03cd0f56cd7d3a0d6130582df33e23cc7abbffd52040198c63b`  
		Last Modified: Mon, 18 Aug 2025 18:43:46 GMT  
		Size: 7.4 MB (7412869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a837a45583444abb61e51c9abe4f0f365a6651d473a1735baf8354bcb87453fc`  
		Last Modified: Mon, 18 Aug 2025 18:43:47 GMT  
		Size: 15.8 KB (15790 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.1.1561-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f3b33921f5b655b5b7c661033a9d00b7b34781a0117df17207cd7c8dbebe9abd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.0 MB (223991139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acbbf1a1028517ee392b624539fa0ae49044efb8bbbb721da4f9aea5b6336a07`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d1e40442030765a3ac5d135c39154d052eba20953ea0e5d35a066f7722cdd93d`  
		Last Modified: Tue, 12 Aug 2025 22:12:36 GMT  
		Size: 49.6 MB (49641603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3eb89d12affa8d8ae917d4a7451665386ed8fa42334a8c26fd85c84363bf134`  
		Last Modified: Mon, 18 Aug 2025 17:24:18 GMT  
		Size: 89.1 MB (89092502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad4e32d1c07dfb2924aef4989ad9f3c804e8b9f9bf92b320f2103a0a9f6db55`  
		Last Modified: Mon, 18 Aug 2025 17:24:18 GMT  
		Size: 85.3 MB (85255990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369b17b4700c54c0217319706ee44b8586ced48a903e22ac8b0e2594e150e259`  
		Last Modified: Mon, 18 Aug 2025 17:24:11 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca86adc67383af7c1161cbae1eaef8f8267a4e39a0078afc24daf746ea6da64b`  
		Last Modified: Mon, 18 Aug 2025 17:24:11 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1561-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:40a2134b6bb2502da004a21549fdb5c1c6c30deb9dfdac69d2797d78cede854f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7435803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e31bf41c06209b9b9a376083df48806ce0c9ddc4dc8fe6a4f4291cf5504e4f33`

```dockerfile
```

-	Layers:
	-	`sha256:0dcf702b5c32100b39479795656dda41d19df0866a7b91a9c9d899d8a76fe73d`  
		Last Modified: Mon, 18 Aug 2025 18:43:53 GMT  
		Size: 7.4 MB (7419896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18962e422683150e652e864243672481cfd2b252190395a56447c58a7be413c3`  
		Last Modified: Mon, 18 Aug 2025 18:43:54 GMT  
		Size: 15.9 KB (15907 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.1.1561-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:796e02ca498542c8921a7482bcc625dd6cfadf07231edd5cb27a0dc889532ff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233863326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53308efdbab9668deb0b32a67db7d44f9c954eb7bed47100f6f5c0711d78b4e0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:befe77620590f63939f5bcadadc9f45832981822c9c901f057eb4e86f733c29a`  
		Last Modified: Wed, 13 Aug 2025 00:32:04 GMT  
		Size: 53.1 MB (53103384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a529d6ce1cfbf7646307577f9dff0071c9dbed24a6448f852c9d01fc20271a0`  
		Last Modified: Mon, 18 Aug 2025 17:40:19 GMT  
		Size: 89.9 MB (89918259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c396f8f2bec2c4a676a06f6a56965a70d1b09f9e654b130c5b90cc9169fec65a`  
		Last Modified: Mon, 18 Aug 2025 17:40:23 GMT  
		Size: 90.8 MB (90840641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dcb1c8b057ad4a5438947a28e602698a022a8fcbaf164aa333f2afe0b51a53f`  
		Last Modified: Mon, 18 Aug 2025 17:40:09 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d07d40b28876c2b1ca7fc4d378e73373e3cb0052fc177deac4b961dc610980eb`  
		Last Modified: Mon, 18 Aug 2025 17:40:09 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1561-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:2e90eab795486e932bcec4e38157de7de1e780cde9be55a4d76c849e8d9bf8b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7434424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b251be5ed2331fcbaa94117532decf06a68c19b0078954d179865491bf6dee2`

```dockerfile
```

-	Layers:
	-	`sha256:b15f4693e879b4e65ac46b1dfb8846459eb115da4d10e62edbdd9405a183b279`  
		Last Modified: Mon, 18 Aug 2025 18:44:00 GMT  
		Size: 7.4 MB (7418586 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7008cfabdb52cd23b4c96dc425a64513c432bc03517b181771deea013dfcf7b`  
		Last Modified: Mon, 18 Aug 2025 18:44:01 GMT  
		Size: 15.8 KB (15838 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.1.1561-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:57a96c9203fa55826cfd3f3d9ddef87980b29bd4c6b45a60e5076a13d8556765
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.8 MB (219760916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:367ac4687a6ea6796430e88ca8733bca57a636d68f926764b0673dd1c037f7cc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:59f3e0adb655cb03f7d489f3cc57e302e249916bbb076c78008f9329238bfb20`  
		Last Modified: Wed, 13 Aug 2025 01:13:55 GMT  
		Size: 47.8 MB (47764303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d3c2b6d6d08922e7d9501bfee1be5dc23cd7a0ba7350b50e7d2e85a3bb3a6fe`  
		Last Modified: Fri, 22 Aug 2025 01:13:06 GMT  
		Size: 87.7 MB (87670398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a3e361a1b825723f158066b69610e428946d264c51a9ee6f3a3fcf0fc28b1a`  
		Last Modified: Fri, 22 Aug 2025 01:13:06 GMT  
		Size: 84.3 MB (84325170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c878dd86e19f678e25289e0923a62caf65e4392c8317cb8f6cfef273f31b540e`  
		Last Modified: Fri, 22 Aug 2025 01:12:54 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd6b27d7397d4b5f4541414ee954147f21b5320b8650d2a56182afd7236367cd`  
		Last Modified: Fri, 22 Aug 2025 01:12:54 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1561-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:1a5d56d3479db952210c8d4f10a5579b007db3b2ed265bfa01c0d939f038469f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7416617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:450b898008fbd9cf1078080f7d75b7e581ca99bfc45e0fed773f730309a13550`

```dockerfile
```

-	Layers:
	-	`sha256:706fcd1c32fc5e5b1861a68d413846478146613b5edd55ec4aa85044170ba29c`  
		Last Modified: Fri, 22 Aug 2025 03:37:44 GMT  
		Size: 7.4 MB (7400779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37cb9174bc9b1d222697f13b21a45576fdcd6dfdf7be2caccb1ee2871aaebb4d`  
		Last Modified: Fri, 22 Aug 2025 03:37:45 GMT  
		Size: 15.8 KB (15838 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.1.1561-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:3d0353a7f5ed940da67ff53c4758e76ce384caf0604b0b9f5e43bb15709ecc65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.0 MB (220976720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5b3ac278d6a328a9d0671b6d31a3d98819060e30da5ae1ee74ba1b7eb43d1ba`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c3b791adea90b39bc59919a9959b7f44f65aa3364a03dd0271a5ff658488877f`  
		Last Modified: Tue, 12 Aug 2025 20:59:03 GMT  
		Size: 49.3 MB (49345161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c850ecedf25d70fc1070e9bc8d02ff404d52931fb1c7f11dbf72f9adc7e94a84`  
		Last Modified: Mon, 18 Aug 2025 18:23:55 GMT  
		Size: 85.2 MB (85226411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0afadace29cf5f56c17c325e7536b76b76abe268020a364c51c3dca96ed2ccb8`  
		Last Modified: Mon, 18 Aug 2025 18:23:53 GMT  
		Size: 86.4 MB (86404103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f890933d1d3855d47e4649ebe6ffa916f39d60926a100281c9442a48b89bfe59`  
		Last Modified: Mon, 18 Aug 2025 18:23:43 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11129af5940006c98ee5ae2cdeeef1fbdb486dc8a2347b0c556fbbb604b6c631`  
		Last Modified: Mon, 18 Aug 2025 18:23:43 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1561-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f3be6b1ece5e81e2958583753dbb41bbbe41141352420608f7d45b336587b08f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7427129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aea4c49637fcd70223f7906ef76de7536f938acd6644a8e78a81b94076343dfd`

```dockerfile
```

-	Layers:
	-	`sha256:0d5b5c88690ae9c02045dada74f6a752354f99a8a974865b420105a7202c6f70`  
		Last Modified: Mon, 18 Aug 2025 21:37:00 GMT  
		Size: 7.4 MB (7411339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4de5dd068cb6aaaaabaf06dc29398cc28c9e00ace1a81da859d137265afa5e6`  
		Last Modified: Mon, 18 Aug 2025 21:37:01 GMT  
		Size: 15.8 KB (15790 bytes)  
		MIME: application/vnd.in-toto+json
