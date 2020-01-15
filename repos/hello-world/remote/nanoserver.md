## `hello-world:nanoserver`

```console
$ docker pull hello-world@sha256:dddb1bb4b4099c0541cd1c313158c3235e7313ded9c571d868b006ae108fe540
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.973; amd64

### `hello-world:nanoserver` - windows version 10.0.17763.973; amd64

```console
$ docker pull hello-world@sha256:707f5243236cda04d8a85dca2a84127adafde76a20f3b75ca4be9e5989ab1591
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.1 MB (101056940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42514ac01c56b846e3cd4048906feb58139b843a2c4fb77ae0803e697abd08b9`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Sat, 04 Jan 2020 07:17:17 GMT
RUN Apply image 1809-amd64
# Wed, 15 Jan 2020 13:11:24 GMT
RUN cmd /S /C #(nop) COPY file:0afaffc2fa64462107b7178b2ae7d20404ff12f637eabe3a8046192b9d9a0338 in C: 
# Wed, 15 Jan 2020 13:11:25 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:ee446884f7bef76f8275c2f16add1c4fb598bea2ba861e72bce8fb4aac9b55ef`  
		Size: 101.1 MB (101054324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8b4475a48151ae7fc0617c015764689f64aeda6768164d3a77d9df00a3189054`  
		Last Modified: Wed, 15 Jan 2020 13:11:44 GMT  
		Size: 1.7 KB (1672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c57688e630a0065a6f44c271f86291ad4f7218c7b93983074e7bdc6247932d5`  
		Last Modified: Wed, 15 Jan 2020 13:11:44 GMT  
		Size: 944.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
