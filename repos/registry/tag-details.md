<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `registry`

-	[`registry:2`](#registry2)
-	[`registry:2.8`](#registry28)
-	[`registry:2.8.3`](#registry283)
-	[`registry:3.0.0-alpha.1`](#registry300-alpha1)
-	[`registry:latest`](#registrylatest)

## `registry:2`

```console
$ docker pull registry@sha256:38d1c1547140226c00be05dc89cbf0862269f12a808a22d4f399d4413513a9e3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `registry:2` - linux; amd64

```console
$ docker pull registry@sha256:97479ff6bb309b6f667458d9f3391dbd1ba87a3d5c4a1b486570ae87e8261a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10111636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a3edb1d5eb6923955548ab7f391e5cc2f04e929c3d32447a7480d8b7a87a0b2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:aa183dc07d0f6a47c02f7f1388fa0ce4639ad328111172149be7c7c65d634ded in / 
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:73baa7ef167e70f1c0233fe09e741780d780ea16e78b3c1b6f4216e2afbbd03e`  
		Last Modified: Thu, 20 Jun 2024 20:17:53 GMT  
		Size: 3.4 MB (3413894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d490907166411a51582f8f9bb5efa7a4f3dffeba3cfeb432a1bb86bcf3e40c77`  
		Last Modified: Thu, 20 Jun 2024 20:56:02 GMT  
		Size: 293.4 KB (293373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8f2b8a18ff7d043b424e13bb9a942587ea819d18ba3823aff5375b92115815`  
		Last Modified: Thu, 20 Jun 2024 20:56:03 GMT  
		Size: 6.4 MB (6403785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d41963883ad33a376d1b2d0ad4b2bdc45a6fbe9531e95324ce476b769e82c52`  
		Last Modified: Thu, 20 Jun 2024 20:56:02 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad02dd2076d659eaac7ce8995ca97151e70196bf3c7ffa6fe3f5f59aa0da96eb`  
		Last Modified: Thu, 20 Jun 2024 20:56:02 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2` - unknown; unknown

```console
$ docker pull registry@sha256:63c6d9ec427e37346c35f2a0f2f1474e4a8d23e49e514f5e7b8df1114182a203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.1 KB (189080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa1fd022de1de96143891948bb6ff8698ecbf9e9a2e851bb792e4ed3437e358a`

```dockerfile
```

-	Layers:
	-	`sha256:945dc0138af5f8fd304e0a62b2728da575027980125b7f0854738ab8caa67d99`  
		Last Modified: Thu, 20 Jun 2024 20:56:02 GMT  
		Size: 175.3 KB (175278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:daff06b9bac2985d18acc823c4ec30bb389a6afe1de0dc80842f0c27dfd1dfff`  
		Last Modified: Thu, 20 Jun 2024 20:56:02 GMT  
		Size: 13.8 KB (13802 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2` - linux; arm variant v6

```console
$ docker pull registry@sha256:35a0b2995ce19cec4145450c06c9686c1c67b2fa267abdcbcd8a7c2f110a3baf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9465795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6f565b2ac702e01f51a256e482e6253ff1bb7e70555f81d6b59aeb6054a7925`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d0c94c425074f8d7a913dd0ec3d0993f0fc85b2f1b727074cde5f8fa967d04`  
		Last Modified: Tue, 30 Apr 2024 17:53:39 GMT  
		Size: 294.0 KB (294045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb0224e4eb15eba3b5f7a7e60f28ccd6d5e5ea52427f424a5915829f32145e0`  
		Last Modified: Tue, 30 Apr 2024 17:53:57 GMT  
		Size: 6.0 MB (6024107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e263264902a4077605fa3ecd524392620904c614aac2aae811c9351fa206546`  
		Last Modified: Tue, 30 Apr 2024 17:53:57 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a33ea41a0bb31a75cf0fa73b3890267569513bc755c56484a11ebb05ae9c7377`  
		Last Modified: Tue, 30 Apr 2024 17:53:57 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2` - unknown; unknown

```console
$ docker pull registry@sha256:66e2f95d8bbb1a44d1ca0fb7e97544a3d2d285601bd7a8707fc3e4bb792bb0f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 KB (13617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43fe79314fe5062b3a9f331a7248f032a3105b8ef478bd93e71dff17856882bf`

```dockerfile
```

-	Layers:
	-	`sha256:af7cf6a5d68f4b3d585c8bfceabe3657deb9c48df32c90e7842ac7f512649117`  
		Last Modified: Tue, 30 Apr 2024 17:53:57 GMT  
		Size: 13.6 KB (13617 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2` - linux; arm variant v7

```console
$ docker pull registry@sha256:c09e4ef41d2b8cb5bea99f451ee5e3d1a11eb0ef7a58f931a789f06c59f81d89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9212158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:788adba0a67bc48a0357a5ad0494f7b1f0f031b4c2cedf90050d9993a2d99428`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ca5dcebc75220c5588066d773a41c8c945a12e7dc046cfd23ee7ec58619aa32`  
		Last Modified: Tue, 30 Apr 2024 18:03:11 GMT  
		Size: 293.0 KB (292967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94055f5852781489c59ebdb17a452b226ddf16b1df78118d30baeff4579c0305`  
		Last Modified: Tue, 30 Apr 2024 18:03:31 GMT  
		Size: 6.0 MB (6017215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1f30785d894085a68123fb60647b0ca6660bc0a643e8a5094aa3c09b6370531`  
		Last Modified: Tue, 30 Apr 2024 18:03:30 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c70f51ab7faa54d3aafec02e7817bd95bdfd3b0797c7955922e2ba13a689459`  
		Last Modified: Tue, 30 Apr 2024 18:03:30 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2` - unknown; unknown

```console
$ docker pull registry@sha256:d23337b052c84486dcc9c0516041abbf348e6c6ad0456801c95ff6cc71bdfbd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.1 KB (190087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7bade424f527ea888c909209da72197b5564115da2ceb66e8c85ebd536747df`

```dockerfile
```

-	Layers:
	-	`sha256:9186b6ae0b06778d1305d6dcc6396912c2c61b6d0a345402647e9c54d54d67ce`  
		Last Modified: Tue, 30 Apr 2024 18:03:30 GMT  
		Size: 176.3 KB (176251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a22cb42b74e7a27ae764231a1bf69ab60478f195d344b28dcaf7785e48383d13`  
		Last Modified: Tue, 30 Apr 2024 18:03:30 GMT  
		Size: 13.8 KB (13836 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:53ee3286cf0400c2ec957e31594c77439ec959e26ca00c8264c5ce521f7859ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9454531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27031dfcd859912546a3d00ad8ec0579adaa81f85dc9ff6099698a994b688203`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76e2c05bc16cc193218be487e39ac3caae6592d57307aaeb0410a43abfcf4858`  
		Last Modified: Tue, 30 Apr 2024 18:11:39 GMT  
		Size: 295.9 KB (295853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6122473202ea088b18b50b2a1156df1b918803043db153f5cb6add1c30539d`  
		Last Modified: Tue, 30 Apr 2024 18:11:58 GMT  
		Size: 5.8 MB (5824733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b06a7c7f2a2124ea42b973fed091d2da803e4c844f520befb1ca70df254c3f1`  
		Last Modified: Tue, 30 Apr 2024 18:11:57 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2824145f0244c1b3a324cb349f251167c79f18c90d0deee54b55a1e7a4604dad`  
		Last Modified: Tue, 30 Apr 2024 18:11:58 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2` - unknown; unknown

```console
$ docker pull registry@sha256:ddf16b02d59316a6cd9e7e1467f7e3117fbd6424f51262ea824c422551099014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 KB (189989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa7f9db154703cba3c714a2d5116640d2017e5be807331430c60daf1eff8441f`

```dockerfile
```

-	Layers:
	-	`sha256:7a8be2171155d1d5edefa6e9af949ee399b8830b51ac0848ec45173f73f41c5a`  
		Last Modified: Tue, 30 Apr 2024 18:11:57 GMT  
		Size: 176.2 KB (176226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f16163694eff969f7c48d7d2a057ec6c54159f1217b6c13d2ede970a49c386e3`  
		Last Modified: Tue, 30 Apr 2024 18:11:57 GMT  
		Size: 13.8 KB (13763 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2` - linux; ppc64le

```console
$ docker pull registry@sha256:fc73c49e31b437c03ede39ca63899f2f6eeb2819db880193edbbbea3bfa193d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9334552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71e302bb58e34c17efc68e8d91f4d29022ea1e47067051d7763b6db6c120a2d2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3e37e3b0015cae0fc32a46185bb04d80ef7a1876829f2cd8d3e25e0e64258e`  
		Last Modified: Tue, 30 Apr 2024 18:03:14 GMT  
		Size: 296.3 KB (296267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32216f19988810f45b91385afb8580026bdd0cf3df07a36052bbf597fb62f839`  
		Last Modified: Tue, 30 Apr 2024 18:04:29 GMT  
		Size: 5.7 MB (5689215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431d2d9a0f324e3cdd8deaf1aea4faa4faed92cb37c404891f2eaf9f334020ba`  
		Last Modified: Tue, 30 Apr 2024 18:04:28 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:396d9ed95af189dc181972d41f8537449d8eb39dff3c830a3637b5ea639e4e13`  
		Last Modified: Tue, 30 Apr 2024 18:04:29 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2` - unknown; unknown

```console
$ docker pull registry@sha256:7882c3a5064eb829ed873b8c3883b2395aa6db3ed82d9d4ad2d1db9fba168096
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.1 KB (188087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d3a542445c5e2ac2aa63c5322a099bf09a984e3f5a983866c728207f37668d3`

```dockerfile
```

-	Layers:
	-	`sha256:cf2859542ec29c98ff80adaa79a9aa4e92eacef8806ddf5de0fb127f8734f4bd`  
		Last Modified: Tue, 30 Apr 2024 18:04:28 GMT  
		Size: 174.3 KB (174295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53468147f333ac654601869ff4a52895b5f9ec280e6b99a13b0a6f3597ec5a53`  
		Last Modified: Tue, 30 Apr 2024 18:04:28 GMT  
		Size: 13.8 KB (13792 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2` - linux; s390x

```console
$ docker pull registry@sha256:a84825b3ee8d4bfeab7ab0fb9a4893ae9e9bd19590f09edde4b835f3b2a6bb10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9672089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7610cc9b5134032c3006fe91c0111bae98daa6e3755a35dc563e94a5be2a3342`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee22372c95aa515952d82e996ea552219f8b8387e28a7784302551be5e80c1e`  
		Last Modified: Tue, 30 Apr 2024 18:03:10 GMT  
		Size: 293.9 KB (293926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8b9bb64acbc685cba56c4e9edcda4189534db0a66b2b54f27da1440bfbe3c8`  
		Last Modified: Tue, 30 Apr 2024 18:03:45 GMT  
		Size: 6.2 MB (6160049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2a6fa86f86567634ad8fd16d47351ad962259a48cdf8689a168cfa85687d52`  
		Last Modified: Tue, 30 Apr 2024 18:03:44 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce941b533ba0fb8619f71bff1d9098248ca5b054e5787eb4c079aa1fc89fbfc`  
		Last Modified: Tue, 30 Apr 2024 18:03:45 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2` - unknown; unknown

```console
$ docker pull registry@sha256:a46e453e7925f04a3487825874995f0556221da3b526d5f7c654fc695bd5cd11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 KB (188014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:626b1303784713792d93804a728bfc099e72ca8498612473f26f13e6dbfa6681`

```dockerfile
```

-	Layers:
	-	`sha256:427ef25a040582ac19cb182432b0a7147cd5f54ba10b291bced28fd287fd9f6e`  
		Last Modified: Tue, 30 Apr 2024 18:03:44 GMT  
		Size: 174.3 KB (174261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ceb9142e1385ee46cbaca350dc69d6dd0d5d1fe588b6b7714b8164878d20c91`  
		Last Modified: Tue, 30 Apr 2024 18:03:44 GMT  
		Size: 13.8 KB (13753 bytes)  
		MIME: application/vnd.in-toto+json

## `registry:2.8`

```console
$ docker pull registry@sha256:38d1c1547140226c00be05dc89cbf0862269f12a808a22d4f399d4413513a9e3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `registry:2.8` - linux; amd64

```console
$ docker pull registry@sha256:97479ff6bb309b6f667458d9f3391dbd1ba87a3d5c4a1b486570ae87e8261a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10111636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a3edb1d5eb6923955548ab7f391e5cc2f04e929c3d32447a7480d8b7a87a0b2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:aa183dc07d0f6a47c02f7f1388fa0ce4639ad328111172149be7c7c65d634ded in / 
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:73baa7ef167e70f1c0233fe09e741780d780ea16e78b3c1b6f4216e2afbbd03e`  
		Last Modified: Thu, 20 Jun 2024 20:17:53 GMT  
		Size: 3.4 MB (3413894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d490907166411a51582f8f9bb5efa7a4f3dffeba3cfeb432a1bb86bcf3e40c77`  
		Last Modified: Thu, 20 Jun 2024 20:56:02 GMT  
		Size: 293.4 KB (293373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8f2b8a18ff7d043b424e13bb9a942587ea819d18ba3823aff5375b92115815`  
		Last Modified: Thu, 20 Jun 2024 20:56:03 GMT  
		Size: 6.4 MB (6403785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d41963883ad33a376d1b2d0ad4b2bdc45a6fbe9531e95324ce476b769e82c52`  
		Last Modified: Thu, 20 Jun 2024 20:56:02 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad02dd2076d659eaac7ce8995ca97151e70196bf3c7ffa6fe3f5f59aa0da96eb`  
		Last Modified: Thu, 20 Jun 2024 20:56:02 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8` - unknown; unknown

```console
$ docker pull registry@sha256:63c6d9ec427e37346c35f2a0f2f1474e4a8d23e49e514f5e7b8df1114182a203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.1 KB (189080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa1fd022de1de96143891948bb6ff8698ecbf9e9a2e851bb792e4ed3437e358a`

```dockerfile
```

-	Layers:
	-	`sha256:945dc0138af5f8fd304e0a62b2728da575027980125b7f0854738ab8caa67d99`  
		Last Modified: Thu, 20 Jun 2024 20:56:02 GMT  
		Size: 175.3 KB (175278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:daff06b9bac2985d18acc823c4ec30bb389a6afe1de0dc80842f0c27dfd1dfff`  
		Last Modified: Thu, 20 Jun 2024 20:56:02 GMT  
		Size: 13.8 KB (13802 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8` - linux; arm variant v6

```console
$ docker pull registry@sha256:35a0b2995ce19cec4145450c06c9686c1c67b2fa267abdcbcd8a7c2f110a3baf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9465795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6f565b2ac702e01f51a256e482e6253ff1bb7e70555f81d6b59aeb6054a7925`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d0c94c425074f8d7a913dd0ec3d0993f0fc85b2f1b727074cde5f8fa967d04`  
		Last Modified: Tue, 30 Apr 2024 17:53:39 GMT  
		Size: 294.0 KB (294045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb0224e4eb15eba3b5f7a7e60f28ccd6d5e5ea52427f424a5915829f32145e0`  
		Last Modified: Tue, 30 Apr 2024 17:53:57 GMT  
		Size: 6.0 MB (6024107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e263264902a4077605fa3ecd524392620904c614aac2aae811c9351fa206546`  
		Last Modified: Tue, 30 Apr 2024 17:53:57 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a33ea41a0bb31a75cf0fa73b3890267569513bc755c56484a11ebb05ae9c7377`  
		Last Modified: Tue, 30 Apr 2024 17:53:57 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8` - unknown; unknown

```console
$ docker pull registry@sha256:66e2f95d8bbb1a44d1ca0fb7e97544a3d2d285601bd7a8707fc3e4bb792bb0f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 KB (13617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43fe79314fe5062b3a9f331a7248f032a3105b8ef478bd93e71dff17856882bf`

```dockerfile
```

-	Layers:
	-	`sha256:af7cf6a5d68f4b3d585c8bfceabe3657deb9c48df32c90e7842ac7f512649117`  
		Last Modified: Tue, 30 Apr 2024 17:53:57 GMT  
		Size: 13.6 KB (13617 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8` - linux; arm variant v7

```console
$ docker pull registry@sha256:c09e4ef41d2b8cb5bea99f451ee5e3d1a11eb0ef7a58f931a789f06c59f81d89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9212158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:788adba0a67bc48a0357a5ad0494f7b1f0f031b4c2cedf90050d9993a2d99428`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ca5dcebc75220c5588066d773a41c8c945a12e7dc046cfd23ee7ec58619aa32`  
		Last Modified: Tue, 30 Apr 2024 18:03:11 GMT  
		Size: 293.0 KB (292967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94055f5852781489c59ebdb17a452b226ddf16b1df78118d30baeff4579c0305`  
		Last Modified: Tue, 30 Apr 2024 18:03:31 GMT  
		Size: 6.0 MB (6017215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1f30785d894085a68123fb60647b0ca6660bc0a643e8a5094aa3c09b6370531`  
		Last Modified: Tue, 30 Apr 2024 18:03:30 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c70f51ab7faa54d3aafec02e7817bd95bdfd3b0797c7955922e2ba13a689459`  
		Last Modified: Tue, 30 Apr 2024 18:03:30 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8` - unknown; unknown

```console
$ docker pull registry@sha256:d23337b052c84486dcc9c0516041abbf348e6c6ad0456801c95ff6cc71bdfbd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.1 KB (190087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7bade424f527ea888c909209da72197b5564115da2ceb66e8c85ebd536747df`

```dockerfile
```

-	Layers:
	-	`sha256:9186b6ae0b06778d1305d6dcc6396912c2c61b6d0a345402647e9c54d54d67ce`  
		Last Modified: Tue, 30 Apr 2024 18:03:30 GMT  
		Size: 176.3 KB (176251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a22cb42b74e7a27ae764231a1bf69ab60478f195d344b28dcaf7785e48383d13`  
		Last Modified: Tue, 30 Apr 2024 18:03:30 GMT  
		Size: 13.8 KB (13836 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:53ee3286cf0400c2ec957e31594c77439ec959e26ca00c8264c5ce521f7859ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9454531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27031dfcd859912546a3d00ad8ec0579adaa81f85dc9ff6099698a994b688203`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76e2c05bc16cc193218be487e39ac3caae6592d57307aaeb0410a43abfcf4858`  
		Last Modified: Tue, 30 Apr 2024 18:11:39 GMT  
		Size: 295.9 KB (295853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6122473202ea088b18b50b2a1156df1b918803043db153f5cb6add1c30539d`  
		Last Modified: Tue, 30 Apr 2024 18:11:58 GMT  
		Size: 5.8 MB (5824733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b06a7c7f2a2124ea42b973fed091d2da803e4c844f520befb1ca70df254c3f1`  
		Last Modified: Tue, 30 Apr 2024 18:11:57 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2824145f0244c1b3a324cb349f251167c79f18c90d0deee54b55a1e7a4604dad`  
		Last Modified: Tue, 30 Apr 2024 18:11:58 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8` - unknown; unknown

```console
$ docker pull registry@sha256:ddf16b02d59316a6cd9e7e1467f7e3117fbd6424f51262ea824c422551099014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 KB (189989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa7f9db154703cba3c714a2d5116640d2017e5be807331430c60daf1eff8441f`

```dockerfile
```

-	Layers:
	-	`sha256:7a8be2171155d1d5edefa6e9af949ee399b8830b51ac0848ec45173f73f41c5a`  
		Last Modified: Tue, 30 Apr 2024 18:11:57 GMT  
		Size: 176.2 KB (176226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f16163694eff969f7c48d7d2a057ec6c54159f1217b6c13d2ede970a49c386e3`  
		Last Modified: Tue, 30 Apr 2024 18:11:57 GMT  
		Size: 13.8 KB (13763 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8` - linux; ppc64le

```console
$ docker pull registry@sha256:fc73c49e31b437c03ede39ca63899f2f6eeb2819db880193edbbbea3bfa193d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9334552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71e302bb58e34c17efc68e8d91f4d29022ea1e47067051d7763b6db6c120a2d2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3e37e3b0015cae0fc32a46185bb04d80ef7a1876829f2cd8d3e25e0e64258e`  
		Last Modified: Tue, 30 Apr 2024 18:03:14 GMT  
		Size: 296.3 KB (296267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32216f19988810f45b91385afb8580026bdd0cf3df07a36052bbf597fb62f839`  
		Last Modified: Tue, 30 Apr 2024 18:04:29 GMT  
		Size: 5.7 MB (5689215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431d2d9a0f324e3cdd8deaf1aea4faa4faed92cb37c404891f2eaf9f334020ba`  
		Last Modified: Tue, 30 Apr 2024 18:04:28 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:396d9ed95af189dc181972d41f8537449d8eb39dff3c830a3637b5ea639e4e13`  
		Last Modified: Tue, 30 Apr 2024 18:04:29 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8` - unknown; unknown

```console
$ docker pull registry@sha256:7882c3a5064eb829ed873b8c3883b2395aa6db3ed82d9d4ad2d1db9fba168096
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.1 KB (188087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d3a542445c5e2ac2aa63c5322a099bf09a984e3f5a983866c728207f37668d3`

```dockerfile
```

-	Layers:
	-	`sha256:cf2859542ec29c98ff80adaa79a9aa4e92eacef8806ddf5de0fb127f8734f4bd`  
		Last Modified: Tue, 30 Apr 2024 18:04:28 GMT  
		Size: 174.3 KB (174295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53468147f333ac654601869ff4a52895b5f9ec280e6b99a13b0a6f3597ec5a53`  
		Last Modified: Tue, 30 Apr 2024 18:04:28 GMT  
		Size: 13.8 KB (13792 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8` - linux; s390x

```console
$ docker pull registry@sha256:a84825b3ee8d4bfeab7ab0fb9a4893ae9e9bd19590f09edde4b835f3b2a6bb10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9672089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7610cc9b5134032c3006fe91c0111bae98daa6e3755a35dc563e94a5be2a3342`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee22372c95aa515952d82e996ea552219f8b8387e28a7784302551be5e80c1e`  
		Last Modified: Tue, 30 Apr 2024 18:03:10 GMT  
		Size: 293.9 KB (293926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8b9bb64acbc685cba56c4e9edcda4189534db0a66b2b54f27da1440bfbe3c8`  
		Last Modified: Tue, 30 Apr 2024 18:03:45 GMT  
		Size: 6.2 MB (6160049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2a6fa86f86567634ad8fd16d47351ad962259a48cdf8689a168cfa85687d52`  
		Last Modified: Tue, 30 Apr 2024 18:03:44 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce941b533ba0fb8619f71bff1d9098248ca5b054e5787eb4c079aa1fc89fbfc`  
		Last Modified: Tue, 30 Apr 2024 18:03:45 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8` - unknown; unknown

```console
$ docker pull registry@sha256:a46e453e7925f04a3487825874995f0556221da3b526d5f7c654fc695bd5cd11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 KB (188014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:626b1303784713792d93804a728bfc099e72ca8498612473f26f13e6dbfa6681`

```dockerfile
```

-	Layers:
	-	`sha256:427ef25a040582ac19cb182432b0a7147cd5f54ba10b291bced28fd287fd9f6e`  
		Last Modified: Tue, 30 Apr 2024 18:03:44 GMT  
		Size: 174.3 KB (174261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ceb9142e1385ee46cbaca350dc69d6dd0d5d1fe588b6b7714b8164878d20c91`  
		Last Modified: Tue, 30 Apr 2024 18:03:44 GMT  
		Size: 13.8 KB (13753 bytes)  
		MIME: application/vnd.in-toto+json

## `registry:2.8.3`

```console
$ docker pull registry@sha256:38d1c1547140226c00be05dc89cbf0862269f12a808a22d4f399d4413513a9e3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `registry:2.8.3` - linux; amd64

```console
$ docker pull registry@sha256:97479ff6bb309b6f667458d9f3391dbd1ba87a3d5c4a1b486570ae87e8261a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10111636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a3edb1d5eb6923955548ab7f391e5cc2f04e929c3d32447a7480d8b7a87a0b2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:aa183dc07d0f6a47c02f7f1388fa0ce4639ad328111172149be7c7c65d634ded in / 
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:73baa7ef167e70f1c0233fe09e741780d780ea16e78b3c1b6f4216e2afbbd03e`  
		Last Modified: Thu, 20 Jun 2024 20:17:53 GMT  
		Size: 3.4 MB (3413894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d490907166411a51582f8f9bb5efa7a4f3dffeba3cfeb432a1bb86bcf3e40c77`  
		Last Modified: Thu, 20 Jun 2024 20:56:02 GMT  
		Size: 293.4 KB (293373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8f2b8a18ff7d043b424e13bb9a942587ea819d18ba3823aff5375b92115815`  
		Last Modified: Thu, 20 Jun 2024 20:56:03 GMT  
		Size: 6.4 MB (6403785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d41963883ad33a376d1b2d0ad4b2bdc45a6fbe9531e95324ce476b769e82c52`  
		Last Modified: Thu, 20 Jun 2024 20:56:02 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad02dd2076d659eaac7ce8995ca97151e70196bf3c7ffa6fe3f5f59aa0da96eb`  
		Last Modified: Thu, 20 Jun 2024 20:56:02 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8.3` - unknown; unknown

```console
$ docker pull registry@sha256:63c6d9ec427e37346c35f2a0f2f1474e4a8d23e49e514f5e7b8df1114182a203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.1 KB (189080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa1fd022de1de96143891948bb6ff8698ecbf9e9a2e851bb792e4ed3437e358a`

```dockerfile
```

-	Layers:
	-	`sha256:945dc0138af5f8fd304e0a62b2728da575027980125b7f0854738ab8caa67d99`  
		Last Modified: Thu, 20 Jun 2024 20:56:02 GMT  
		Size: 175.3 KB (175278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:daff06b9bac2985d18acc823c4ec30bb389a6afe1de0dc80842f0c27dfd1dfff`  
		Last Modified: Thu, 20 Jun 2024 20:56:02 GMT  
		Size: 13.8 KB (13802 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8.3` - linux; arm variant v6

```console
$ docker pull registry@sha256:35a0b2995ce19cec4145450c06c9686c1c67b2fa267abdcbcd8a7c2f110a3baf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9465795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6f565b2ac702e01f51a256e482e6253ff1bb7e70555f81d6b59aeb6054a7925`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d0c94c425074f8d7a913dd0ec3d0993f0fc85b2f1b727074cde5f8fa967d04`  
		Last Modified: Tue, 30 Apr 2024 17:53:39 GMT  
		Size: 294.0 KB (294045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb0224e4eb15eba3b5f7a7e60f28ccd6d5e5ea52427f424a5915829f32145e0`  
		Last Modified: Tue, 30 Apr 2024 17:53:57 GMT  
		Size: 6.0 MB (6024107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e263264902a4077605fa3ecd524392620904c614aac2aae811c9351fa206546`  
		Last Modified: Tue, 30 Apr 2024 17:53:57 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a33ea41a0bb31a75cf0fa73b3890267569513bc755c56484a11ebb05ae9c7377`  
		Last Modified: Tue, 30 Apr 2024 17:53:57 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8.3` - unknown; unknown

```console
$ docker pull registry@sha256:66e2f95d8bbb1a44d1ca0fb7e97544a3d2d285601bd7a8707fc3e4bb792bb0f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 KB (13617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43fe79314fe5062b3a9f331a7248f032a3105b8ef478bd93e71dff17856882bf`

```dockerfile
```

-	Layers:
	-	`sha256:af7cf6a5d68f4b3d585c8bfceabe3657deb9c48df32c90e7842ac7f512649117`  
		Last Modified: Tue, 30 Apr 2024 17:53:57 GMT  
		Size: 13.6 KB (13617 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8.3` - linux; arm variant v7

```console
$ docker pull registry@sha256:c09e4ef41d2b8cb5bea99f451ee5e3d1a11eb0ef7a58f931a789f06c59f81d89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9212158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:788adba0a67bc48a0357a5ad0494f7b1f0f031b4c2cedf90050d9993a2d99428`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ca5dcebc75220c5588066d773a41c8c945a12e7dc046cfd23ee7ec58619aa32`  
		Last Modified: Tue, 30 Apr 2024 18:03:11 GMT  
		Size: 293.0 KB (292967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94055f5852781489c59ebdb17a452b226ddf16b1df78118d30baeff4579c0305`  
		Last Modified: Tue, 30 Apr 2024 18:03:31 GMT  
		Size: 6.0 MB (6017215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1f30785d894085a68123fb60647b0ca6660bc0a643e8a5094aa3c09b6370531`  
		Last Modified: Tue, 30 Apr 2024 18:03:30 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c70f51ab7faa54d3aafec02e7817bd95bdfd3b0797c7955922e2ba13a689459`  
		Last Modified: Tue, 30 Apr 2024 18:03:30 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8.3` - unknown; unknown

```console
$ docker pull registry@sha256:d23337b052c84486dcc9c0516041abbf348e6c6ad0456801c95ff6cc71bdfbd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.1 KB (190087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7bade424f527ea888c909209da72197b5564115da2ceb66e8c85ebd536747df`

```dockerfile
```

-	Layers:
	-	`sha256:9186b6ae0b06778d1305d6dcc6396912c2c61b6d0a345402647e9c54d54d67ce`  
		Last Modified: Tue, 30 Apr 2024 18:03:30 GMT  
		Size: 176.3 KB (176251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a22cb42b74e7a27ae764231a1bf69ab60478f195d344b28dcaf7785e48383d13`  
		Last Modified: Tue, 30 Apr 2024 18:03:30 GMT  
		Size: 13.8 KB (13836 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8.3` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:53ee3286cf0400c2ec957e31594c77439ec959e26ca00c8264c5ce521f7859ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9454531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27031dfcd859912546a3d00ad8ec0579adaa81f85dc9ff6099698a994b688203`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76e2c05bc16cc193218be487e39ac3caae6592d57307aaeb0410a43abfcf4858`  
		Last Modified: Tue, 30 Apr 2024 18:11:39 GMT  
		Size: 295.9 KB (295853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6122473202ea088b18b50b2a1156df1b918803043db153f5cb6add1c30539d`  
		Last Modified: Tue, 30 Apr 2024 18:11:58 GMT  
		Size: 5.8 MB (5824733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b06a7c7f2a2124ea42b973fed091d2da803e4c844f520befb1ca70df254c3f1`  
		Last Modified: Tue, 30 Apr 2024 18:11:57 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2824145f0244c1b3a324cb349f251167c79f18c90d0deee54b55a1e7a4604dad`  
		Last Modified: Tue, 30 Apr 2024 18:11:58 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8.3` - unknown; unknown

```console
$ docker pull registry@sha256:ddf16b02d59316a6cd9e7e1467f7e3117fbd6424f51262ea824c422551099014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 KB (189989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa7f9db154703cba3c714a2d5116640d2017e5be807331430c60daf1eff8441f`

```dockerfile
```

-	Layers:
	-	`sha256:7a8be2171155d1d5edefa6e9af949ee399b8830b51ac0848ec45173f73f41c5a`  
		Last Modified: Tue, 30 Apr 2024 18:11:57 GMT  
		Size: 176.2 KB (176226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f16163694eff969f7c48d7d2a057ec6c54159f1217b6c13d2ede970a49c386e3`  
		Last Modified: Tue, 30 Apr 2024 18:11:57 GMT  
		Size: 13.8 KB (13763 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8.3` - linux; ppc64le

```console
$ docker pull registry@sha256:fc73c49e31b437c03ede39ca63899f2f6eeb2819db880193edbbbea3bfa193d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9334552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71e302bb58e34c17efc68e8d91f4d29022ea1e47067051d7763b6db6c120a2d2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3e37e3b0015cae0fc32a46185bb04d80ef7a1876829f2cd8d3e25e0e64258e`  
		Last Modified: Tue, 30 Apr 2024 18:03:14 GMT  
		Size: 296.3 KB (296267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32216f19988810f45b91385afb8580026bdd0cf3df07a36052bbf597fb62f839`  
		Last Modified: Tue, 30 Apr 2024 18:04:29 GMT  
		Size: 5.7 MB (5689215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431d2d9a0f324e3cdd8deaf1aea4faa4faed92cb37c404891f2eaf9f334020ba`  
		Last Modified: Tue, 30 Apr 2024 18:04:28 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:396d9ed95af189dc181972d41f8537449d8eb39dff3c830a3637b5ea639e4e13`  
		Last Modified: Tue, 30 Apr 2024 18:04:29 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8.3` - unknown; unknown

```console
$ docker pull registry@sha256:7882c3a5064eb829ed873b8c3883b2395aa6db3ed82d9d4ad2d1db9fba168096
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.1 KB (188087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d3a542445c5e2ac2aa63c5322a099bf09a984e3f5a983866c728207f37668d3`

```dockerfile
```

-	Layers:
	-	`sha256:cf2859542ec29c98ff80adaa79a9aa4e92eacef8806ddf5de0fb127f8734f4bd`  
		Last Modified: Tue, 30 Apr 2024 18:04:28 GMT  
		Size: 174.3 KB (174295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53468147f333ac654601869ff4a52895b5f9ec280e6b99a13b0a6f3597ec5a53`  
		Last Modified: Tue, 30 Apr 2024 18:04:28 GMT  
		Size: 13.8 KB (13792 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8.3` - linux; s390x

```console
$ docker pull registry@sha256:a84825b3ee8d4bfeab7ab0fb9a4893ae9e9bd19590f09edde4b835f3b2a6bb10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9672089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7610cc9b5134032c3006fe91c0111bae98daa6e3755a35dc563e94a5be2a3342`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee22372c95aa515952d82e996ea552219f8b8387e28a7784302551be5e80c1e`  
		Last Modified: Tue, 30 Apr 2024 18:03:10 GMT  
		Size: 293.9 KB (293926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8b9bb64acbc685cba56c4e9edcda4189534db0a66b2b54f27da1440bfbe3c8`  
		Last Modified: Tue, 30 Apr 2024 18:03:45 GMT  
		Size: 6.2 MB (6160049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2a6fa86f86567634ad8fd16d47351ad962259a48cdf8689a168cfa85687d52`  
		Last Modified: Tue, 30 Apr 2024 18:03:44 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce941b533ba0fb8619f71bff1d9098248ca5b054e5787eb4c079aa1fc89fbfc`  
		Last Modified: Tue, 30 Apr 2024 18:03:45 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8.3` - unknown; unknown

```console
$ docker pull registry@sha256:a46e453e7925f04a3487825874995f0556221da3b526d5f7c654fc695bd5cd11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 KB (188014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:626b1303784713792d93804a728bfc099e72ca8498612473f26f13e6dbfa6681`

```dockerfile
```

-	Layers:
	-	`sha256:427ef25a040582ac19cb182432b0a7147cd5f54ba10b291bced28fd287fd9f6e`  
		Last Modified: Tue, 30 Apr 2024 18:03:44 GMT  
		Size: 174.3 KB (174261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ceb9142e1385ee46cbaca350dc69d6dd0d5d1fe588b6b7714b8164878d20c91`  
		Last Modified: Tue, 30 Apr 2024 18:03:44 GMT  
		Size: 13.8 KB (13753 bytes)  
		MIME: application/vnd.in-toto+json

## `registry:3.0.0-alpha.1`

```console
$ docker pull registry@sha256:69cd2f2b12c67b82d1f32510bfc97bb00e101c4c76bfd60f1ef824f5fbd69118
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `registry:3.0.0-alpha.1` - linux; amd64

```console
$ docker pull registry@sha256:f81e277b902d07c4958ea3c7197e60d5165f788f1122f4da15cf750915f8c233
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 MB (14227375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc8bd2463b7aa3dd5f16c2273acab73b4845c8e500eecc96852e61cf8b61d853`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 19 Dec 2023 16:37:37 GMT
ADD file:aa183dc07d0f6a47c02f7f1388fa0ce4639ad328111172149be7c7c65d634ded in / 
# Tue, 19 Dec 2023 16:37:37 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 16:37:37 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 19 Dec 2023 16:37:37 GMT
RUN set -eux; 	version='3.0.0-alpha.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='968a6dcc648aa842963ae00a28128200b6134732ff73db6fc1e52c6f9099d1f9' ;; 		aarch64) arch='arm64';   sha256='4f0d3ab06b8f77abf5ae39f08a214c2451b9eec4b1b9bb2eb9b9b9da3a3ad4cf' ;; 		armhf)   arch='armv6';   sha256='5ac4ac9cd5c7c658cd719efc44a67a0ef4b03e0618aa359ae726938eade66300' ;; 		armv7)   arch='armv7';   sha256='3c2eb167a162a17453dee0e43fb97b5abb771decf60b492e2867a2354fd0618d' ;; 		ppc64le) arch='ppc64le'; sha256='1e39ce43428437faf31f5df636d94c4dc21958076ebf96c1bd3baf67c3f7199a' ;; 		s390x)   arch='s390x';   sha256='94c53ba2254013b3e38d0c0a8d8005e41681f1f394c23a61db9953d61c134c07' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Tue, 19 Dec 2023 16:37:37 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Tue, 19 Dec 2023 16:37:37 GMT
VOLUME [/var/lib/registry]
# Tue, 19 Dec 2023 16:37:37 GMT
EXPOSE map[5000/tcp:{}]
# Tue, 19 Dec 2023 16:37:37 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Dec 2023 16:37:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Dec 2023 16:37:37 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:73baa7ef167e70f1c0233fe09e741780d780ea16e78b3c1b6f4216e2afbbd03e`  
		Last Modified: Thu, 20 Jun 2024 20:17:53 GMT  
		Size: 3.4 MB (3413894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c6d1270bb225221a153af79aff12dc32e789f4d92422539d1be94ae588fcba`  
		Last Modified: Thu, 20 Jun 2024 20:55:58 GMT  
		Size: 293.4 KB (293367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e6fdd5c51aea5598edca216ed6012cbc7d6effb1672a55180965a4b87cc747a`  
		Last Modified: Thu, 20 Jun 2024 20:55:58 GMT  
		Size: 10.5 MB (10519529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d02916a0c0722bc525fef2008e2fa182929af35f8fd9529b425b4d337f2714`  
		Last Modified: Thu, 20 Jun 2024 20:55:58 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5379317961932fb8b1d41f78289cef5a0eacf4fbc923da1412d54cafc283e573`  
		Last Modified: Thu, 20 Jun 2024 20:55:58 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-alpha.1` - unknown; unknown

```console
$ docker pull registry@sha256:0d73f5ce8d6f85be7ad50b20fd730fc5381d580ad9c67b47124dcbd9199b7cb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.0 KB (243985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:075b66ac307c215fc1fa8949a55b6c034c095c5f72a03fd7c8393531e23f8965`

```dockerfile
```

-	Layers:
	-	`sha256:20b93925ee23a11f66f706ed8d7f4eea8bd063ce25453b2b542edd33378d45d5`  
		Last Modified: Thu, 20 Jun 2024 20:55:58 GMT  
		Size: 231.0 KB (231038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a187fbcc779301a238e3c0aca368edd8cbd513d3ea367ca274eb41ecec5c7b09`  
		Last Modified: Thu, 20 Jun 2024 20:55:58 GMT  
		Size: 12.9 KB (12947 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0-alpha.1` - linux; arm variant v6

```console
$ docker pull registry@sha256:1624913fe3764b26cd268b231063a9ea217e65b5c15df8515ec718114a28f5c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13406702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f198ca552f16b7424cefc7ab6f4db0c18d2f0d3bfd53530e3dcba70100a2d1c3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 19 Dec 2023 16:37:37 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Tue, 19 Dec 2023 16:37:37 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 16:37:37 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 19 Dec 2023 16:37:37 GMT
RUN set -eux; 	version='3.0.0-alpha.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='968a6dcc648aa842963ae00a28128200b6134732ff73db6fc1e52c6f9099d1f9' ;; 		aarch64) arch='arm64';   sha256='4f0d3ab06b8f77abf5ae39f08a214c2451b9eec4b1b9bb2eb9b9b9da3a3ad4cf' ;; 		armhf)   arch='armv6';   sha256='5ac4ac9cd5c7c658cd719efc44a67a0ef4b03e0618aa359ae726938eade66300' ;; 		armv7)   arch='armv7';   sha256='3c2eb167a162a17453dee0e43fb97b5abb771decf60b492e2867a2354fd0618d' ;; 		ppc64le) arch='ppc64le'; sha256='1e39ce43428437faf31f5df636d94c4dc21958076ebf96c1bd3baf67c3f7199a' ;; 		s390x)   arch='s390x';   sha256='94c53ba2254013b3e38d0c0a8d8005e41681f1f394c23a61db9953d61c134c07' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Tue, 19 Dec 2023 16:37:37 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Tue, 19 Dec 2023 16:37:37 GMT
VOLUME [/var/lib/registry]
# Tue, 19 Dec 2023 16:37:37 GMT
EXPOSE map[5000/tcp:{}]
# Tue, 19 Dec 2023 16:37:37 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Dec 2023 16:37:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Dec 2023 16:37:37 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d0c94c425074f8d7a913dd0ec3d0993f0fc85b2f1b727074cde5f8fa967d04`  
		Last Modified: Tue, 30 Apr 2024 17:53:39 GMT  
		Size: 294.0 KB (294045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c293b5ad228027b21b2eb51fa829346ce439022b86030633282880ba7c0efbb`  
		Last Modified: Tue, 30 Apr 2024 17:53:39 GMT  
		Size: 10.0 MB (9965016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22939b24742a399e6b34a1aee7b48e0719ca7c29e592275091965032fa3a96f4`  
		Last Modified: Tue, 30 Apr 2024 17:53:38 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f07a6f8b66d0d2a705baf1e0e055cb6d15206a162e9353c84a6818fac206e02`  
		Last Modified: Tue, 30 Apr 2024 17:53:39 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-alpha.1` - unknown; unknown

```console
$ docker pull registry@sha256:c06c4cf7a430e13104412767a3d6586f7f2f80709eba962444ad98db9040723b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 KB (12901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4100da958708b4c3834231518522f67318e2dd0b1bcecdb065f83df0247c93d`

```dockerfile
```

-	Layers:
	-	`sha256:4b3394b81704a3381bb7607af12939bd68d2208dfd45c98f6372a9f35ab2267b`  
		Last Modified: Tue, 30 Apr 2024 17:53:39 GMT  
		Size: 12.9 KB (12901 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0-alpha.1` - linux; arm variant v7

```console
$ docker pull registry@sha256:584773cb1d186257bbcb385fea9f88041fbdf7e7e52e7a603a510eb13296b9d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13149485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0ed5c79fe9298fafa52ab1acc7c1b2fc1a76dd44b0dfdc6ae33f9c904890d01`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 19 Dec 2023 16:37:37 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Tue, 19 Dec 2023 16:37:37 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 16:37:37 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 19 Dec 2023 16:37:37 GMT
RUN set -eux; 	version='3.0.0-alpha.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='968a6dcc648aa842963ae00a28128200b6134732ff73db6fc1e52c6f9099d1f9' ;; 		aarch64) arch='arm64';   sha256='4f0d3ab06b8f77abf5ae39f08a214c2451b9eec4b1b9bb2eb9b9b9da3a3ad4cf' ;; 		armhf)   arch='armv6';   sha256='5ac4ac9cd5c7c658cd719efc44a67a0ef4b03e0618aa359ae726938eade66300' ;; 		armv7)   arch='armv7';   sha256='3c2eb167a162a17453dee0e43fb97b5abb771decf60b492e2867a2354fd0618d' ;; 		ppc64le) arch='ppc64le'; sha256='1e39ce43428437faf31f5df636d94c4dc21958076ebf96c1bd3baf67c3f7199a' ;; 		s390x)   arch='s390x';   sha256='94c53ba2254013b3e38d0c0a8d8005e41681f1f394c23a61db9953d61c134c07' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Tue, 19 Dec 2023 16:37:37 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Tue, 19 Dec 2023 16:37:37 GMT
VOLUME [/var/lib/registry]
# Tue, 19 Dec 2023 16:37:37 GMT
EXPOSE map[5000/tcp:{}]
# Tue, 19 Dec 2023 16:37:37 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Dec 2023 16:37:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Dec 2023 16:37:37 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ca5dcebc75220c5588066d773a41c8c945a12e7dc046cfd23ee7ec58619aa32`  
		Last Modified: Tue, 30 Apr 2024 18:03:11 GMT  
		Size: 293.0 KB (292967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bd8e25b92c8b2b43e9602cc7847fd89832c789b5f12a1014c5151aedeb4d388`  
		Last Modified: Tue, 30 Apr 2024 18:03:11 GMT  
		Size: 10.0 MB (9954543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fab98f8a4426fadce1b4fa5826e8abd3c89a8232cbdc422b2617a7e80ed4a3`  
		Last Modified: Tue, 30 Apr 2024 18:03:11 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3a01969b2adcfbed53de756b58dece8f54dca8b5779a3b023200cb8972b315`  
		Last Modified: Tue, 30 Apr 2024 18:03:10 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-alpha.1` - unknown; unknown

```console
$ docker pull registry@sha256:bc409cea20cb6687bc6e6ff7e1454b724fd8b2828e1544aea5736599c4a9b712
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.0 KB (244997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37688a21b5b3656e3e11269e521d10bd2e1215309f4ddefdb86337dcd938b2af`

```dockerfile
```

-	Layers:
	-	`sha256:cd24b94f70d7affb6078be1535eb6600054ef75de553d4347c80348c73a1a6fc`  
		Last Modified: Tue, 30 Apr 2024 18:03:11 GMT  
		Size: 232.0 KB (232043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e6d1f1700c98e809ab5946378e4b476d8e6432f8c6e7cb26eb9bcccc1264e9a`  
		Last Modified: Tue, 30 Apr 2024 18:03:11 GMT  
		Size: 13.0 KB (12954 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0-alpha.1` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:34da24570ee5b24bdc1b877b19a55f7ec0ab703191462f31579813387a38099c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13359297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d778abef82338feae0d9254e5094b0880ed145364c6fa3a26f7e9e9490c58c6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 19 Dec 2023 16:37:37 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Tue, 19 Dec 2023 16:37:37 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 16:37:37 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 19 Dec 2023 16:37:37 GMT
RUN set -eux; 	version='3.0.0-alpha.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='968a6dcc648aa842963ae00a28128200b6134732ff73db6fc1e52c6f9099d1f9' ;; 		aarch64) arch='arm64';   sha256='4f0d3ab06b8f77abf5ae39f08a214c2451b9eec4b1b9bb2eb9b9b9da3a3ad4cf' ;; 		armhf)   arch='armv6';   sha256='5ac4ac9cd5c7c658cd719efc44a67a0ef4b03e0618aa359ae726938eade66300' ;; 		armv7)   arch='armv7';   sha256='3c2eb167a162a17453dee0e43fb97b5abb771decf60b492e2867a2354fd0618d' ;; 		ppc64le) arch='ppc64le'; sha256='1e39ce43428437faf31f5df636d94c4dc21958076ebf96c1bd3baf67c3f7199a' ;; 		s390x)   arch='s390x';   sha256='94c53ba2254013b3e38d0c0a8d8005e41681f1f394c23a61db9953d61c134c07' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Tue, 19 Dec 2023 16:37:37 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Tue, 19 Dec 2023 16:37:37 GMT
VOLUME [/var/lib/registry]
# Tue, 19 Dec 2023 16:37:37 GMT
EXPOSE map[5000/tcp:{}]
# Tue, 19 Dec 2023 16:37:37 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Dec 2023 16:37:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Dec 2023 16:37:37 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76e2c05bc16cc193218be487e39ac3caae6592d57307aaeb0410a43abfcf4858`  
		Last Modified: Tue, 30 Apr 2024 18:11:39 GMT  
		Size: 295.9 KB (295853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9eff81ad0e0d3e54e75ac8699fa57250ccdffb3e1423f949eecb43ab970d4bf`  
		Last Modified: Tue, 30 Apr 2024 18:11:39 GMT  
		Size: 9.7 MB (9729499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb81767643ceb4eb7f50971e02c8dbe6ce1b059c4e1e46fbdfd75e1cab201dca`  
		Last Modified: Tue, 30 Apr 2024 18:11:39 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684c60f5b60781e6b400b7c8a4f32f99be1419f1d7b192fd81563e7f3363e684`  
		Last Modified: Tue, 30 Apr 2024 18:11:39 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-alpha.1` - unknown; unknown

```console
$ docker pull registry@sha256:dd9252a76d5a983c2d42099f7f738d7e485d69a45418739007edadbf4b378ea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.1 KB (245101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:782ebe62110362fef8e52bea5d10107350340afb21c4a514dec7513ac57e58a3`

```dockerfile
```

-	Layers:
	-	`sha256:f563b5da49926bb19f9172209704e5b07c48f4055497fdb1060ca57d8e8f6273`  
		Last Modified: Tue, 30 Apr 2024 18:11:39 GMT  
		Size: 232.0 KB (232036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:986524ae23863b5f82aec03c19dbb9daf46d5853a39bd87bd2f80fd00d1d8c6e`  
		Last Modified: Tue, 30 Apr 2024 18:11:39 GMT  
		Size: 13.1 KB (13065 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0-alpha.1` - linux; ppc64le

```console
$ docker pull registry@sha256:4f383bbd6bb8623f3666adea8449a55937a088c87428e5c5a73a1d84669e85c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13119898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7047b15f517f6e542dd3fa088213fce951dccba8f3eafec13b1da1501fcf4a1f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 19 Dec 2023 16:37:37 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Tue, 19 Dec 2023 16:37:37 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 16:37:37 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 19 Dec 2023 16:37:37 GMT
RUN set -eux; 	version='3.0.0-alpha.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='968a6dcc648aa842963ae00a28128200b6134732ff73db6fc1e52c6f9099d1f9' ;; 		aarch64) arch='arm64';   sha256='4f0d3ab06b8f77abf5ae39f08a214c2451b9eec4b1b9bb2eb9b9b9da3a3ad4cf' ;; 		armhf)   arch='armv6';   sha256='5ac4ac9cd5c7c658cd719efc44a67a0ef4b03e0618aa359ae726938eade66300' ;; 		armv7)   arch='armv7';   sha256='3c2eb167a162a17453dee0e43fb97b5abb771decf60b492e2867a2354fd0618d' ;; 		ppc64le) arch='ppc64le'; sha256='1e39ce43428437faf31f5df636d94c4dc21958076ebf96c1bd3baf67c3f7199a' ;; 		s390x)   arch='s390x';   sha256='94c53ba2254013b3e38d0c0a8d8005e41681f1f394c23a61db9953d61c134c07' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Tue, 19 Dec 2023 16:37:37 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Tue, 19 Dec 2023 16:37:37 GMT
VOLUME [/var/lib/registry]
# Tue, 19 Dec 2023 16:37:37 GMT
EXPOSE map[5000/tcp:{}]
# Tue, 19 Dec 2023 16:37:37 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Dec 2023 16:37:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Dec 2023 16:37:37 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3e37e3b0015cae0fc32a46185bb04d80ef7a1876829f2cd8d3e25e0e64258e`  
		Last Modified: Tue, 30 Apr 2024 18:03:14 GMT  
		Size: 296.3 KB (296267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc412b7c9e10efbe4ac199547e3c1b89166254a5bb0f966ed98d26c4e9d9e877`  
		Last Modified: Tue, 30 Apr 2024 18:03:15 GMT  
		Size: 9.5 MB (9474562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4bc9c0c23f0d9f504657e66182093342b895f8b7b14cc3fb00e5791e54f04e`  
		Last Modified: Tue, 30 Apr 2024 18:03:14 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87352e77db3ab3a38437e528aac93d9b033cb87dbfdbcf1dd79a2f4d7005321f`  
		Last Modified: Tue, 30 Apr 2024 18:03:14 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-alpha.1` - unknown; unknown

```console
$ docker pull registry@sha256:42b7514c0d1022376cd54bf9b59b4ed6c51c815596912609834266c4e9bdcb95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.0 KB (243008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9daac1c29b7742c93712a49c27bcc76615474e8b064c8d516c7ca97e7f2beed`

```dockerfile
```

-	Layers:
	-	`sha256:a198c35cf9d021686ac437718547581fd1372119d63cd3b9afe79fc31408bd28`  
		Last Modified: Tue, 30 Apr 2024 18:03:14 GMT  
		Size: 230.1 KB (230093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90e76c4c0a08aa4a62a17de4a7df52860052cab24976e0360860d42493f5ad66`  
		Last Modified: Tue, 30 Apr 2024 18:03:14 GMT  
		Size: 12.9 KB (12915 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0-alpha.1` - linux; s390x

```console
$ docker pull registry@sha256:6a2dfc4f8bf1ee9e6e98800ed25421362fa4600be7e539dd7ae79c51e231dcc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13607236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ab2d65926dfcf8b7a86d38dcecb8e94b119db4ec587843a963719af5e6e4ca0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 19 Dec 2023 16:37:37 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Tue, 19 Dec 2023 16:37:37 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 16:37:37 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 19 Dec 2023 16:37:37 GMT
RUN set -eux; 	version='3.0.0-alpha.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='968a6dcc648aa842963ae00a28128200b6134732ff73db6fc1e52c6f9099d1f9' ;; 		aarch64) arch='arm64';   sha256='4f0d3ab06b8f77abf5ae39f08a214c2451b9eec4b1b9bb2eb9b9b9da3a3ad4cf' ;; 		armhf)   arch='armv6';   sha256='5ac4ac9cd5c7c658cd719efc44a67a0ef4b03e0618aa359ae726938eade66300' ;; 		armv7)   arch='armv7';   sha256='3c2eb167a162a17453dee0e43fb97b5abb771decf60b492e2867a2354fd0618d' ;; 		ppc64le) arch='ppc64le'; sha256='1e39ce43428437faf31f5df636d94c4dc21958076ebf96c1bd3baf67c3f7199a' ;; 		s390x)   arch='s390x';   sha256='94c53ba2254013b3e38d0c0a8d8005e41681f1f394c23a61db9953d61c134c07' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Tue, 19 Dec 2023 16:37:37 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Tue, 19 Dec 2023 16:37:37 GMT
VOLUME [/var/lib/registry]
# Tue, 19 Dec 2023 16:37:37 GMT
EXPOSE map[5000/tcp:{}]
# Tue, 19 Dec 2023 16:37:37 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Dec 2023 16:37:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Dec 2023 16:37:37 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee22372c95aa515952d82e996ea552219f8b8387e28a7784302551be5e80c1e`  
		Last Modified: Tue, 30 Apr 2024 18:03:10 GMT  
		Size: 293.9 KB (293926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52802b36c2c9b8932d59d0ebd90d1f453e5f9c0210066ac84c8e061cc2ec44e`  
		Last Modified: Tue, 30 Apr 2024 18:03:11 GMT  
		Size: 10.1 MB (10095198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf999ea11e68e638d9ee953093b99a308e29d508c425e2bb7f654415a2abfdd1`  
		Last Modified: Tue, 30 Apr 2024 18:03:10 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd45c40919a75ae0003a28738a802dee7d443613130aa476855a8c820aca790`  
		Last Modified: Tue, 30 Apr 2024 18:03:10 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-alpha.1` - unknown; unknown

```console
$ docker pull registry@sha256:0cf782c42693dd05d7509ea1ac4e87adb40ec48c87408a62fbe2ed0ccaa28d4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.9 KB (242903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48797bd5ad8b073a63fd04d015393fd850e735d358049ca3dbd9ba92a1fe772`

```dockerfile
```

-	Layers:
	-	`sha256:ef5301998a04cd86c66a667a292c6277aa0236809f6bd8fe6ebd22a19b23c5fc`  
		Last Modified: Tue, 30 Apr 2024 18:03:10 GMT  
		Size: 230.0 KB (230005 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a99e5b0ac785eacde29b074732531cc117ea4279e4202cab5b395bcee878269`  
		Last Modified: Tue, 30 Apr 2024 18:03:10 GMT  
		Size: 12.9 KB (12898 bytes)  
		MIME: application/vnd.in-toto+json

## `registry:latest`

```console
$ docker pull registry@sha256:38d1c1547140226c00be05dc89cbf0862269f12a808a22d4f399d4413513a9e3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `registry:latest` - linux; amd64

```console
$ docker pull registry@sha256:97479ff6bb309b6f667458d9f3391dbd1ba87a3d5c4a1b486570ae87e8261a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10111636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a3edb1d5eb6923955548ab7f391e5cc2f04e929c3d32447a7480d8b7a87a0b2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:aa183dc07d0f6a47c02f7f1388fa0ce4639ad328111172149be7c7c65d634ded in / 
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:73baa7ef167e70f1c0233fe09e741780d780ea16e78b3c1b6f4216e2afbbd03e`  
		Last Modified: Thu, 20 Jun 2024 20:17:53 GMT  
		Size: 3.4 MB (3413894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d490907166411a51582f8f9bb5efa7a4f3dffeba3cfeb432a1bb86bcf3e40c77`  
		Last Modified: Thu, 20 Jun 2024 20:56:02 GMT  
		Size: 293.4 KB (293373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8f2b8a18ff7d043b424e13bb9a942587ea819d18ba3823aff5375b92115815`  
		Last Modified: Thu, 20 Jun 2024 20:56:03 GMT  
		Size: 6.4 MB (6403785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d41963883ad33a376d1b2d0ad4b2bdc45a6fbe9531e95324ce476b769e82c52`  
		Last Modified: Thu, 20 Jun 2024 20:56:02 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad02dd2076d659eaac7ce8995ca97151e70196bf3c7ffa6fe3f5f59aa0da96eb`  
		Last Modified: Thu, 20 Jun 2024 20:56:02 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:63c6d9ec427e37346c35f2a0f2f1474e4a8d23e49e514f5e7b8df1114182a203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.1 KB (189080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa1fd022de1de96143891948bb6ff8698ecbf9e9a2e851bb792e4ed3437e358a`

```dockerfile
```

-	Layers:
	-	`sha256:945dc0138af5f8fd304e0a62b2728da575027980125b7f0854738ab8caa67d99`  
		Last Modified: Thu, 20 Jun 2024 20:56:02 GMT  
		Size: 175.3 KB (175278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:daff06b9bac2985d18acc823c4ec30bb389a6afe1de0dc80842f0c27dfd1dfff`  
		Last Modified: Thu, 20 Jun 2024 20:56:02 GMT  
		Size: 13.8 KB (13802 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; arm variant v6

```console
$ docker pull registry@sha256:35a0b2995ce19cec4145450c06c9686c1c67b2fa267abdcbcd8a7c2f110a3baf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9465795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6f565b2ac702e01f51a256e482e6253ff1bb7e70555f81d6b59aeb6054a7925`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d0c94c425074f8d7a913dd0ec3d0993f0fc85b2f1b727074cde5f8fa967d04`  
		Last Modified: Tue, 30 Apr 2024 17:53:39 GMT  
		Size: 294.0 KB (294045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb0224e4eb15eba3b5f7a7e60f28ccd6d5e5ea52427f424a5915829f32145e0`  
		Last Modified: Tue, 30 Apr 2024 17:53:57 GMT  
		Size: 6.0 MB (6024107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e263264902a4077605fa3ecd524392620904c614aac2aae811c9351fa206546`  
		Last Modified: Tue, 30 Apr 2024 17:53:57 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a33ea41a0bb31a75cf0fa73b3890267569513bc755c56484a11ebb05ae9c7377`  
		Last Modified: Tue, 30 Apr 2024 17:53:57 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:66e2f95d8bbb1a44d1ca0fb7e97544a3d2d285601bd7a8707fc3e4bb792bb0f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 KB (13617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43fe79314fe5062b3a9f331a7248f032a3105b8ef478bd93e71dff17856882bf`

```dockerfile
```

-	Layers:
	-	`sha256:af7cf6a5d68f4b3d585c8bfceabe3657deb9c48df32c90e7842ac7f512649117`  
		Last Modified: Tue, 30 Apr 2024 17:53:57 GMT  
		Size: 13.6 KB (13617 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; arm variant v7

```console
$ docker pull registry@sha256:c09e4ef41d2b8cb5bea99f451ee5e3d1a11eb0ef7a58f931a789f06c59f81d89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9212158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:788adba0a67bc48a0357a5ad0494f7b1f0f031b4c2cedf90050d9993a2d99428`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ca5dcebc75220c5588066d773a41c8c945a12e7dc046cfd23ee7ec58619aa32`  
		Last Modified: Tue, 30 Apr 2024 18:03:11 GMT  
		Size: 293.0 KB (292967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94055f5852781489c59ebdb17a452b226ddf16b1df78118d30baeff4579c0305`  
		Last Modified: Tue, 30 Apr 2024 18:03:31 GMT  
		Size: 6.0 MB (6017215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1f30785d894085a68123fb60647b0ca6660bc0a643e8a5094aa3c09b6370531`  
		Last Modified: Tue, 30 Apr 2024 18:03:30 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c70f51ab7faa54d3aafec02e7817bd95bdfd3b0797c7955922e2ba13a689459`  
		Last Modified: Tue, 30 Apr 2024 18:03:30 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:d23337b052c84486dcc9c0516041abbf348e6c6ad0456801c95ff6cc71bdfbd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.1 KB (190087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7bade424f527ea888c909209da72197b5564115da2ceb66e8c85ebd536747df`

```dockerfile
```

-	Layers:
	-	`sha256:9186b6ae0b06778d1305d6dcc6396912c2c61b6d0a345402647e9c54d54d67ce`  
		Last Modified: Tue, 30 Apr 2024 18:03:30 GMT  
		Size: 176.3 KB (176251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a22cb42b74e7a27ae764231a1bf69ab60478f195d344b28dcaf7785e48383d13`  
		Last Modified: Tue, 30 Apr 2024 18:03:30 GMT  
		Size: 13.8 KB (13836 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:53ee3286cf0400c2ec957e31594c77439ec959e26ca00c8264c5ce521f7859ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9454531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27031dfcd859912546a3d00ad8ec0579adaa81f85dc9ff6099698a994b688203`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76e2c05bc16cc193218be487e39ac3caae6592d57307aaeb0410a43abfcf4858`  
		Last Modified: Tue, 30 Apr 2024 18:11:39 GMT  
		Size: 295.9 KB (295853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6122473202ea088b18b50b2a1156df1b918803043db153f5cb6add1c30539d`  
		Last Modified: Tue, 30 Apr 2024 18:11:58 GMT  
		Size: 5.8 MB (5824733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b06a7c7f2a2124ea42b973fed091d2da803e4c844f520befb1ca70df254c3f1`  
		Last Modified: Tue, 30 Apr 2024 18:11:57 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2824145f0244c1b3a324cb349f251167c79f18c90d0deee54b55a1e7a4604dad`  
		Last Modified: Tue, 30 Apr 2024 18:11:58 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:ddf16b02d59316a6cd9e7e1467f7e3117fbd6424f51262ea824c422551099014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 KB (189989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa7f9db154703cba3c714a2d5116640d2017e5be807331430c60daf1eff8441f`

```dockerfile
```

-	Layers:
	-	`sha256:7a8be2171155d1d5edefa6e9af949ee399b8830b51ac0848ec45173f73f41c5a`  
		Last Modified: Tue, 30 Apr 2024 18:11:57 GMT  
		Size: 176.2 KB (176226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f16163694eff969f7c48d7d2a057ec6c54159f1217b6c13d2ede970a49c386e3`  
		Last Modified: Tue, 30 Apr 2024 18:11:57 GMT  
		Size: 13.8 KB (13763 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; ppc64le

```console
$ docker pull registry@sha256:fc73c49e31b437c03ede39ca63899f2f6eeb2819db880193edbbbea3bfa193d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9334552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71e302bb58e34c17efc68e8d91f4d29022ea1e47067051d7763b6db6c120a2d2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3e37e3b0015cae0fc32a46185bb04d80ef7a1876829f2cd8d3e25e0e64258e`  
		Last Modified: Tue, 30 Apr 2024 18:03:14 GMT  
		Size: 296.3 KB (296267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32216f19988810f45b91385afb8580026bdd0cf3df07a36052bbf597fb62f839`  
		Last Modified: Tue, 30 Apr 2024 18:04:29 GMT  
		Size: 5.7 MB (5689215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431d2d9a0f324e3cdd8deaf1aea4faa4faed92cb37c404891f2eaf9f334020ba`  
		Last Modified: Tue, 30 Apr 2024 18:04:28 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:396d9ed95af189dc181972d41f8537449d8eb39dff3c830a3637b5ea639e4e13`  
		Last Modified: Tue, 30 Apr 2024 18:04:29 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:7882c3a5064eb829ed873b8c3883b2395aa6db3ed82d9d4ad2d1db9fba168096
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.1 KB (188087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d3a542445c5e2ac2aa63c5322a099bf09a984e3f5a983866c728207f37668d3`

```dockerfile
```

-	Layers:
	-	`sha256:cf2859542ec29c98ff80adaa79a9aa4e92eacef8806ddf5de0fb127f8734f4bd`  
		Last Modified: Tue, 30 Apr 2024 18:04:28 GMT  
		Size: 174.3 KB (174295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53468147f333ac654601869ff4a52895b5f9ec280e6b99a13b0a6f3597ec5a53`  
		Last Modified: Tue, 30 Apr 2024 18:04:28 GMT  
		Size: 13.8 KB (13792 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; s390x

```console
$ docker pull registry@sha256:a84825b3ee8d4bfeab7ab0fb9a4893ae9e9bd19590f09edde4b835f3b2a6bb10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9672089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7610cc9b5134032c3006fe91c0111bae98daa6e3755a35dc563e94a5be2a3342`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee22372c95aa515952d82e996ea552219f8b8387e28a7784302551be5e80c1e`  
		Last Modified: Tue, 30 Apr 2024 18:03:10 GMT  
		Size: 293.9 KB (293926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8b9bb64acbc685cba56c4e9edcda4189534db0a66b2b54f27da1440bfbe3c8`  
		Last Modified: Tue, 30 Apr 2024 18:03:45 GMT  
		Size: 6.2 MB (6160049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2a6fa86f86567634ad8fd16d47351ad962259a48cdf8689a168cfa85687d52`  
		Last Modified: Tue, 30 Apr 2024 18:03:44 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce941b533ba0fb8619f71bff1d9098248ca5b054e5787eb4c079aa1fc89fbfc`  
		Last Modified: Tue, 30 Apr 2024 18:03:45 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:a46e453e7925f04a3487825874995f0556221da3b526d5f7c654fc695bd5cd11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 KB (188014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:626b1303784713792d93804a728bfc099e72ca8498612473f26f13e6dbfa6681`

```dockerfile
```

-	Layers:
	-	`sha256:427ef25a040582ac19cb182432b0a7147cd5f54ba10b291bced28fd287fd9f6e`  
		Last Modified: Tue, 30 Apr 2024 18:03:44 GMT  
		Size: 174.3 KB (174261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ceb9142e1385ee46cbaca350dc69d6dd0d5d1fe588b6b7714b8164878d20c91`  
		Last Modified: Tue, 30 Apr 2024 18:03:44 GMT  
		Size: 13.8 KB (13753 bytes)  
		MIME: application/vnd.in-toto+json
