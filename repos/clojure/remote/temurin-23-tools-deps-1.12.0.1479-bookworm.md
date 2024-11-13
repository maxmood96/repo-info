## `clojure:temurin-23-tools-deps-1.12.0.1479-bookworm`

```console
$ docker pull clojure@sha256:0e1550487a153ecd579aaa3bb502f48bc005f3b7c900ce24b04456bd7379e971
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-1.12.0.1479-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:c9021a801d8205197e102ccb4af648fb718812ea22d10fe47bc2ebf3351896d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.8 MB (295810229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a2b11dff752dc0e929594a0146bda0b392cace75bb8404ed49076a77c2a2ea7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1d21051c4640be8d92999d473d97f5b00c12b3772eec17dd5b9709bed43750`  
		Last Modified: Tue, 12 Nov 2024 02:50:22 GMT  
		Size: 165.3 MB (165295128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc5c24209ae10874a53d6679d1df47ac7f05009047792d5bf5ab31c71bed003`  
		Last Modified: Tue, 12 Nov 2024 02:50:21 GMT  
		Size: 80.9 MB (80938369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:516ece4db3e9a7b9b854c8fe865802d346e37c9a98e4a7e2f45e2593d60bd1a3`  
		Last Modified: Tue, 12 Nov 2024 02:50:17 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf37d98cf0921a429a673d782dcabca6f1fba146631b34c63f587b44f7f3d94e`  
		Last Modified: Tue, 12 Nov 2024 02:50:17 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1479-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:d1cceb74c70634828f2bbbcef00e76d8e31aed8f402cbdb7303cbc66e33d205e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7204624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6335c150dbea9919cfc237f3126da7971f67bb0081ed88ded164dc2761bdcb0`

```dockerfile
```

-	Layers:
	-	`sha256:d8891de5e254e54fd3e142b53c9c636e625c72582b75088e9c9d407e6b53cdd1`  
		Last Modified: Tue, 12 Nov 2024 02:50:18 GMT  
		Size: 7.2 MB (7188120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b704b4f6b57ae262e32069fa6f26fad3e81779844821bc92dc4b303c7e77723c`  
		Last Modified: Tue, 12 Nov 2024 02:50:17 GMT  
		Size: 16.5 KB (16504 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps-1.12.0.1479-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ba8cee405316594d45b0398735d4aace464c6c17a817de042701fd6f1f969912
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.7 MB (293668171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cdcd87f01f3d369ab904764559acf61d3f99aba32236731557c0d3ef18e0ace`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1a3f1864ec54b1398987bbe673e93d8b09842ecd51e86ab87d64857b70d188b1`  
		Last Modified: Tue, 12 Nov 2024 00:56:20 GMT  
		Size: 49.6 MB (49587201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4390a79c18cdc6fa048fb832bf562c2313423d011d581778d6f3b60e31bfba`  
		Last Modified: Wed, 13 Nov 2024 01:33:30 GMT  
		Size: 163.3 MB (163281821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6422410d9f72419ff3f072d8243ba1becaaaa4ad80af40ba34b1173ad9b18fd2`  
		Last Modified: Wed, 13 Nov 2024 01:38:06 GMT  
		Size: 80.8 MB (80798112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99299c64dc85e735ebb45d83c535d5f0bd0882b93f7c278b1064eb7e04d4b96d`  
		Last Modified: Wed, 13 Nov 2024 01:38:04 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064fdddab504eb07b6962c991a9e79bf6b5d132b1140f931b692ce63eac610de`  
		Last Modified: Wed, 13 Nov 2024 01:38:04 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1479-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:4e0b00f0dc9f5508e577c77c3c72db540596d1c591678997623a3866dc3d1099
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7209136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b87ef47424774d365691d1cdd9fa1767e11b6b82f105a8ce522f561de181da41`

```dockerfile
```

-	Layers:
	-	`sha256:f4b2a61107f4ac4f688eaf02c5162e36bf32bec659cfc8f05b509a25083831a7`  
		Last Modified: Wed, 13 Nov 2024 01:38:04 GMT  
		Size: 7.2 MB (7193290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a5ff0fc01d82b6764f2b2032d8fc9c91b724f8c859b2ae968c2ad303279a61d`  
		Last Modified: Wed, 13 Nov 2024 01:38:03 GMT  
		Size: 15.8 KB (15846 bytes)  
		MIME: application/vnd.in-toto+json
