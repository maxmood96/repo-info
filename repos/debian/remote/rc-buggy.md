## `debian:rc-buggy`

```console
$ docker pull debian@sha256:821e5a0e58875ad669c9a990051ad951042c6210ff1995c3eff7a21c87d985ad
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

### `debian:rc-buggy` - linux; amd64

```console
$ docker pull debian@sha256:02fa1142f2a4ff108cc4f5c54421d118c8a63361fb31ab616ec11ffd9ce0da67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48670806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc3a7622d9bbbdfdc65e6ee2d4e30196a8cb75815ddfa60238a87867d2065bcd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1776729600'
# Wed, 22 Apr 2026 01:15:38 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:a10f86d641494b5e6b1c3b8b85409baab7c4d325c9d6b292a94180331dd6b765`  
		Last Modified: Wed, 22 Apr 2026 00:17:03 GMT  
		Size: 48.7 MB (48670580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33f49aa470af2967688adab0dc0212a6e8650392f16e5ca38df5cf8c12fb212`  
		Last Modified: Wed, 22 Apr 2026 01:15:44 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:5de89139edc4bb4cbedff060509fa3808d0ea1d291e44c258d9f279686ad406f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3151586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef8049ce84aef0544a55c79a0e053fd098e6af3b083588e908510bf65be925fe`

```dockerfile
```

-	Layers:
	-	`sha256:705fc22bb6cf9d083ac973afc04e7f164053bc6209f8d5972ee2730e429521ef`  
		Last Modified: Wed, 22 Apr 2026 01:15:44 GMT  
		Size: 3.1 MB (3145531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a268f9f655e08d80807fefabaf007eaf6f7fc6dbfad2a734ebb17e6017c37e1`  
		Last Modified: Wed, 22 Apr 2026 01:15:44 GMT  
		Size: 6.1 KB (6055 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; arm variant v7

```console
$ docker pull debian@sha256:dd87550eb7986856cf826b98e61c195ad5140e418c82f42c44a35638e21af083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45607611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5714ded2176aa4853f0b6c93837ebc67c4d00ddb2da3bc113c0f4ba1ffb046dc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1776729600'
# Wed, 22 Apr 2026 01:15:21 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:954ecf3bb623246e76e048be8db255040be0be61ff8078225017790f93fc2baf`  
		Last Modified: Wed, 22 Apr 2026 00:16:56 GMT  
		Size: 45.6 MB (45607386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18206d2716011a3a1cac727f5b2dab37eddfa7e0fa9b5fd928aef3f06b45c682`  
		Last Modified: Wed, 22 Apr 2026 01:15:26 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:f23ac6b130bec9a29c515cbd24caafa49a2a41309d36430206db587a19d83fbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3153021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f2df831b7c7ab1ec943c56c2f2e5479dd7bffbd7629c5312a97cfbdea15b61f`

```dockerfile
```

-	Layers:
	-	`sha256:99fef03daaed07ab1e7efdc22b5ca9e7de244e3595fe327827c453c44a6702be`  
		Last Modified: Wed, 22 Apr 2026 01:15:27 GMT  
		Size: 3.1 MB (3146901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f740595142e37d6856fc1dc7257b2eedb91538e6ade37a82b91523924c1b321`  
		Last Modified: Wed, 22 Apr 2026 01:15:26 GMT  
		Size: 6.1 KB (6120 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:ca3a9cf7b7afc3b8f64026f9a2ef5258219964ad79ba6f5f99deacdfcfc025f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48711596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c18d6a2794300b682d82df88ff22c7b46ef6b209d5f4b60981d3bcff0d3d955`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1776729600'
# Wed, 22 Apr 2026 01:15:46 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:f7ead27882db0d1de6eb6e496d384f406d278f217abdf3e3c50a235ce7737146`  
		Last Modified: Wed, 22 Apr 2026 00:16:20 GMT  
		Size: 48.7 MB (48711371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4eb5677c955086978473e9ff6208be109125bf85bc257d0b9c7924c63c866ee`  
		Last Modified: Wed, 22 Apr 2026 01:15:53 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:54598297780078a140dd119f6dbba5ecea4f66cd8fef44783b273d3246b7d0bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3157628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76ef98cfc5af29ac3cffb9c440519b5ca713aa26c04622f0dcd1180a53c9c8ef`

```dockerfile
```

-	Layers:
	-	`sha256:f272781743f59f520596408e79a740dc1a765b446ef9eacde68c9c4f2d433474`  
		Last Modified: Wed, 22 Apr 2026 01:15:53 GMT  
		Size: 3.2 MB (3151493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11f4688109b8c2948a94ecd7cb7e0032674137020e8053ffbc5fadf7c122abc9`  
		Last Modified: Wed, 22 Apr 2026 01:15:53 GMT  
		Size: 6.1 KB (6135 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; 386

```console
$ docker pull debian@sha256:aa957ad1eb2df1f7dcb982053f40c9c0372599f8a302c4d77a708cb34d16c9f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49993937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5516b7b522cc4372bd69d333f76949f73e4028a023f391433c1ded0c93f6bcd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1775433600'
# Tue, 07 Apr 2026 01:16:46 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:0c3eef9d9722af9b5785c5725c5b18d448456ee05c327ddf5310134754139706`  
		Last Modified: Tue, 07 Apr 2026 00:11:45 GMT  
		Size: 50.0 MB (49993711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91fceff9acdb4173d3f35bdee073b5fcf9880308e651aa32607e89e8ee556b1a`  
		Last Modified: Tue, 07 Apr 2026 01:16:52 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:1258282deb3695eaa7acb6d0c2b605a02182590f433161d71025897269b9e0f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3143898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78f22a27738a06e386fe79770092df69854f2e350db51c54fb8d4934af735be3`

```dockerfile
```

-	Layers:
	-	`sha256:b86ef5d9d24eb3cbd836878c11a6cea1aefd975774acc7bce0359045822fa7ff`  
		Last Modified: Tue, 07 Apr 2026 01:16:52 GMT  
		Size: 3.1 MB (3137864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f52494423f50e5a4b0efa62068ec6baf9aed96a53d4ce7751b3f9ca800f499d`  
		Last Modified: Tue, 07 Apr 2026 01:16:52 GMT  
		Size: 6.0 KB (6034 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; ppc64le

```console
$ docker pull debian@sha256:7974a240cbcf782995aa1facfef5f634c762036d6290f1a1626da35e5d79a4a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (54002176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61efb99f5cb448761a87d9d5390296274e1ce21d061e62c0c6ac968ce6825ead`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1775433600'
# Tue, 07 Apr 2026 01:17:58 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:8091a6b5ece83586bfb56b6975e0b2d9bc01c78d84b526c5c6e82463bb755232`  
		Last Modified: Tue, 07 Apr 2026 00:11:11 GMT  
		Size: 54.0 MB (54001950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3457d843760c1e6f22c7a23f14d757c91cdaf432689f61dc12fe2e51485eba8b`  
		Last Modified: Tue, 07 Apr 2026 01:18:15 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:cebe37af6457116cb061c4605b2c2065fbc995b93616e7267cadfb786a5c2c78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3150253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cb8e43ab296a1eacf2bffc9105b3b18494bd9eaa9e4c0847948c0c30d0ebaa0`

```dockerfile
```

-	Layers:
	-	`sha256:ee4b70460fc9816d838ddb09547c8fb0784574249b06a75fbcc0bf7c4d3422d3`  
		Last Modified: Tue, 07 Apr 2026 01:18:15 GMT  
		Size: 3.1 MB (3144165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f74c0f9a687067b244068f783498a0496af4c02900bfcc997d59bfc7a750684`  
		Last Modified: Tue, 07 Apr 2026 01:18:15 GMT  
		Size: 6.1 KB (6088 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; riscv64

```console
$ docker pull debian@sha256:994d721701c7606336c0a312fcbf01e5729bdd8c99feda7cb73e63ff1394b923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46787132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7bd437e03283a0907b4432a46682ba24ef50648a144f80ce805052fbde8d78e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1775433600'
# Tue, 07 Apr 2026 02:36:23 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:fd96dd3de127541ef7e3bc5f9bc63bfe49b8f35d0526495ebca95ce89fe40405`  
		Last Modified: Tue, 07 Apr 2026 01:43:52 GMT  
		Size: 46.8 MB (46786906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4470304d8ffca39558e5c298821aa200080b81acc7f40cffb82383a7ceff98`  
		Last Modified: Tue, 07 Apr 2026 02:37:15 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:ce740996ea38579e45c72da859b0e2bc55f63b01abe93d6a523ad46a64844b73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3138256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1175131b4a958d085719e718d753f4322cb56b226b245b635415ae37180cbb9`

```dockerfile
```

-	Layers:
	-	`sha256:4dca5c6cc6f7caa0b394ff779ed3c3473a6b030f33222e9170c7c5efa29f6227`  
		Last Modified: Tue, 07 Apr 2026 02:37:16 GMT  
		Size: 3.1 MB (3132168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea482b53cd31b712287a23dbbc822fd37717f4ce2732c7d52b2c93505c2d3a66`  
		Last Modified: Tue, 07 Apr 2026 02:37:15 GMT  
		Size: 6.1 KB (6088 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; s390x

```console
$ docker pull debian@sha256:e6f97b29560087029294e3145381cf78d97cde97cd1c5ef89890d80ca38ea97d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48411176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba534234b544a140fbb89d86d1515b047ced9b1e474ef8bbc6bc19204e6fc1b4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1776729600'
# Wed, 22 Apr 2026 01:15:07 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:7b993b1f311a8e0a662fe34124c78c97a70f47ef43d775021c60d64af67fe6f9`  
		Last Modified: Wed, 22 Apr 2026 00:16:09 GMT  
		Size: 48.4 MB (48410950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78afe702474b293c33b04bed04dd7f46e76c83f9873773279885d7517714223c`  
		Last Modified: Wed, 22 Apr 2026 01:15:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:2d68ba931459f294e0e3ef777960691e4c57db8501b2c15e7ffe091b1fba4b7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3153038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edeabf82e3604e63c2a01dd68405145acc162f80bb2f5073f798bb5fcc074c94`

```dockerfile
```

-	Layers:
	-	`sha256:c8b1a79b33c98f0d2693fb7e49df70767e0f41dac3f0a3c5bfca4bf5c4ea6356`  
		Last Modified: Wed, 22 Apr 2026 01:15:20 GMT  
		Size: 3.1 MB (3146982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6822944ec4faf2a0246e5948ed21f432ea424cde6a9227cc7076b7c1b601761`  
		Last Modified: Wed, 22 Apr 2026 01:15:20 GMT  
		Size: 6.1 KB (6056 bytes)  
		MIME: application/vnd.in-toto+json
