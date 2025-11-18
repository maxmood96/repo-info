## `debian:forky-backports`

```console
$ docker pull debian@sha256:e792ad4d40a01a3e146c410495e81456c643058aba1e6d9f3dbd4e4cd4a0660f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `debian:forky-backports` - linux; amd64

```console
$ docker pull debian@sha256:193950c20dd20080b13ad0b4edb75b60bb5345f4610a47904afa72dacae11776
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48500658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ca45331eca5f7ea18713f8265a6bc06bf7cf538dc6a09e0689116421da3d9cf`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1763337600'
# Tue, 18 Nov 2025 03:55:10 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:76694dc296168bbffa890c84fb372e9c250bf33e0ad63a6146b169a57d983e2f`  
		Last Modified: Tue, 18 Nov 2025 02:29:31 GMT  
		Size: 48.5 MB (48500434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a834c6cce5faeb3d4b1cc06b10bd92ff4478b882f26346a9667cb363be4a5c74`  
		Last Modified: Tue, 18 Nov 2025 03:55:20 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:da3a9db176f628122b6afc5998618133fedc452b488b29617fad14fce460218e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3135311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cc1141c711d680e09d71311a84eff4db864b28b142af6deedb3fc9ec1c29bcd`

```dockerfile
```

-	Layers:
	-	`sha256:a1f13be9c52659a50cc284471e0ceb02a79e3edcbadaf1718f021c7c90874e32`  
		Last Modified: Tue, 18 Nov 2025 04:28:02 GMT  
		Size: 3.1 MB (3129533 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8698b5f3abae2b9eb867aa876e0154473d798a38fcbb1a7a63b62703719bcdfa`  
		Last Modified: Tue, 18 Nov 2025 04:28:03 GMT  
		Size: 5.8 KB (5778 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:b7194f9b0f5f22489c90fb94005a3b7b2ec7f4d4d60f6781ca0c60eec4478431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (45003983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90bb676a40a6ede704d05047269e16bb61699af335fb2e292ef1688506320c38`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1763337600'
# Tue, 18 Nov 2025 02:16:32 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:1dd1fa3a56d87bf4dcae80a33b02589ad31d81e866bca9f061ada67db33c8854`  
		Last Modified: Tue, 18 Nov 2025 01:12:58 GMT  
		Size: 45.0 MB (45003762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe080826e475ec9da871d0dc5307b4af9c595b2a375eea367c2e2fdba5488c1`  
		Last Modified: Tue, 18 Nov 2025 02:16:44 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:7dbb41f0d9ffb3d25a4badfa49063ecbdabbf7e157d36fcecbd3cc2afaeb5c9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3136735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7750ec20b6bbfe2295b219d5e9b6e0635565da4701ad43143ace02bea8dc3324`

```dockerfile
```

-	Layers:
	-	`sha256:e46a0119a2572b43248de21559629b28356551f8a0e19af359e279d4ed199ad4`  
		Last Modified: Tue, 18 Nov 2025 04:28:07 GMT  
		Size: 3.1 MB (3130901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43b78dfdc726fc26b94c4594322490f952439de4b0989701c6f86332f00baad2`  
		Last Modified: Tue, 18 Nov 2025 04:28:08 GMT  
		Size: 5.8 KB (5834 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:40a2f5112c18822c0123cdfcbf0e8ba3dab0ed66e85324f0e3cfea8ac2c307dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48591407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cf1e6085e0da4b9af4171e0f323e01a669e75dead3ab8c76cba47951a86776d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1763337600'
# Tue, 18 Nov 2025 02:15:37 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:25dea15c4ffeb70e1112f1ee06dd948a8ab9dfc3b79ef239cb96080cc27ff1be`  
		Last Modified: Tue, 18 Nov 2025 01:13:47 GMT  
		Size: 48.6 MB (48591184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:525cf0e6042d0d5e996c12ba22c67d19c0b3db9d0739d036b6368e2ebd8d4262`  
		Last Modified: Tue, 18 Nov 2025 02:15:48 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:f07be029bec5b80957fbf7912e4c24975fd053500cd188bd3d29fed01f4af1b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3136218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:869929ab260970b95ec0c3a6ba4d8d9cffee28f3e1f525945708f9527f3ab89d`

```dockerfile
```

-	Layers:
	-	`sha256:b32c903777da15fdc3815f6ec4cd88a0e3536aa92c621a3eac77d3d4144586fe`  
		Last Modified: Tue, 18 Nov 2025 04:28:15 GMT  
		Size: 3.1 MB (3130374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ddcacf83e44cd26f4e2a6c41d4871a26abf3989c54fd0b9f2b70dd3900fbfe7`  
		Last Modified: Tue, 18 Nov 2025 04:28:21 GMT  
		Size: 5.8 KB (5844 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; 386

```console
$ docker pull debian@sha256:b89cc231528bc86029e92cb0a03ae1764291921121d6e0b2142dac221a6795df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49832460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a201b6b7e42784086f1ff3356209e4b7526b451bb888a60188cd6829d03eea3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1763337600'
# Tue, 18 Nov 2025 02:15:39 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:898cf630ac245ec9ad865c96204520b86bb7b8760d5bd2f14bd02745e43d82f4`  
		Last Modified: Tue, 18 Nov 2025 01:13:40 GMT  
		Size: 49.8 MB (49832238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb4cd47c9c5c4b0fc105c1fecba2752f6b14781d650e3463bc680163110a765`  
		Last Modified: Tue, 18 Nov 2025 02:15:50 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:092ae1c52b09d09a8069bcafc4ea14f27dc17050277c3252aa078b4c9b5b458c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3132503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:523c59999526007262771f20f345a07632ef7c03037b08bcadfee555b5693606`

```dockerfile
```

-	Layers:
	-	`sha256:cee5a134d82cda21470ee5a2f915ab14d4484637cf29c9a608e26bfa9995e209`  
		Last Modified: Tue, 18 Nov 2025 04:28:24 GMT  
		Size: 3.1 MB (3126742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e52fb7dfc84d95a8347ec0ea2cfba4ecd44315e951a3ccf0265db212fd9540ff`  
		Last Modified: Tue, 18 Nov 2025 04:28:25 GMT  
		Size: 5.8 KB (5761 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:6425cc95d1ae65010be2a9a9bda54061b9452540ab14e3b00766bd54a23db20c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53315462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d699cfe7f98864d7e457d98ff887cf6ae7ad1104245dac9cc1c5199c011341`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1762202650'
# Tue, 04 Nov 2025 01:16:38 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:9422d47ff8508a211c5181db20a5b72bab47758f9bcd0687b05752ead1b35a5a`  
		Last Modified: Tue, 04 Nov 2025 00:14:32 GMT  
		Size: 53.3 MB (53315240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c90a0262c729fe506b0910731b6394c72668d5493197ceac363a0d0488cb0347`  
		Last Modified: Tue, 04 Nov 2025 01:17:03 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:366ae5e156e4757b4e659e7613b0f109ce23fdb4428097519012e54cadec882e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3138830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dddea961a3c4b6936eb21cc61a733f87f0c6932e983bf31b6121f6db31cbd7c1`

```dockerfile
```

-	Layers:
	-	`sha256:c457bae33f3451df6a02c04e7bfc75f4c403d4f82eb8a44b78d3484ecfd48145`  
		Last Modified: Tue, 04 Nov 2025 22:33:07 GMT  
		Size: 3.1 MB (3133026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dba6ba587f1a368af75817b0d878229e769259c0d7978f0a42525bfb797e49ac`  
		Last Modified: Tue, 04 Nov 2025 22:33:08 GMT  
		Size: 5.8 KB (5804 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; riscv64

```console
$ docker pull debian@sha256:bd31f1a0f9417d523d70b80bcda53cd4ee8979aa7b615ed1bbe4014a9d719306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46791348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6894dae8e8ab629861fb6dcec1059a67039f705015d549cc0dbf292809d4d6ae`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1762202650'
# Tue, 04 Nov 2025 01:17:59 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:81afe9ed9d72ebbd06999820f64e36aa62bc978725062b4cc32efc39c6a99213`  
		Last Modified: Tue, 04 Nov 2025 00:13:41 GMT  
		Size: 46.8 MB (46791125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf706f26189ec92bd8b1b973e142e9d62839cac2656e3c210a0f6c4338970682`  
		Last Modified: Tue, 04 Nov 2025 01:19:01 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:be7a7e5773769c10b18220a0d8629ff3406a6c62784bafaa265a047170012d94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3127639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad3360a9a5e9b7a38d0f536334ffffbd65592750ec06552934264dc3dc13843f`

```dockerfile
```

-	Layers:
	-	`sha256:1adb4e4fafdb387907e0316874c685c0e3f419ad26201ea9996d7f0bac4732f2`  
		Last Modified: Tue, 04 Nov 2025 07:28:28 GMT  
		Size: 3.1 MB (3121836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b5558d66ad2b4082167870128fd27e7e7a49869b27945952309683c0008e7b3`  
		Last Modified: Tue, 04 Nov 2025 07:28:28 GMT  
		Size: 5.8 KB (5803 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; s390x

```console
$ docker pull debian@sha256:0a41824a191ce1d5c0b3d3186dc4e96bbba9e914551228dbb57d40f4775a1c18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48343286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63d394ac31ffc5cd971211bfb60a238dc975e655f89d7dd61838c167e29c221`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1762202650'
# Tue, 04 Nov 2025 06:40:34 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:aa89048d1c3c931b297cf2d408ea7138528530c43e452af625223e71f97282b3`  
		Last Modified: Tue, 04 Nov 2025 00:14:09 GMT  
		Size: 48.3 MB (48343062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a0a62be9a1e0a60ed7eaa92972c892f1dd4072432b7c10a3b22e65eaeb5cb1d`  
		Last Modified: Tue, 04 Nov 2025 06:40:55 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:2baf7cb6d4258c286627da7e762ca832323e9b18f416369ba9b7a44d29aa16c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3136764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ac72fc038c9d8000b7678c7b3ed039d525dca4fd1eb69b541efb9352bc9378`

```dockerfile
```

-	Layers:
	-	`sha256:58af562d7764045426fd302234b1314e02c5f0c191aa36c041d7b779f182d907`  
		Last Modified: Tue, 18 Nov 2025 04:28:37 GMT  
		Size: 3.1 MB (3130986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:effca480b54a8bec54d287524178b57be37c0f3cd7f150df33bb609cd35cb282`  
		Last Modified: Tue, 18 Nov 2025 04:28:37 GMT  
		Size: 5.8 KB (5778 bytes)  
		MIME: application/vnd.in-toto+json
