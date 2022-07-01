<template>
<section class="homepage-container">

  <nav-bar />
  
  <div class="movies-container">

  <movie-card v-for="movie in movies" :key="movie.index"
  :title="movie.title"
  :year="movie.year"
  :rating="movie.rated"
  :genre="movie.genre[0]"
  :poster="movie.poster"
  />

  </div>
</section>
</template>

<script>
import MovieCard from '../components/Global/MovieCard/MovieCard.vue'
import NavBar from '../components/Global/NavBar/NavBar.vue'

export default {
  name: 'IndexPage',

  components: {
    MovieCard,
    NavBar
  },

  data: () => ({
    movies: [
    {
      title: "Spiderman: No Way Home",
      year: "2019",
      rated: "15",
      runtime: "106 min",
      genre: ['action', 'sci-fi'],
      poster: "https://m.media-amazon.com/images/M/MV5BZWMyYzFjYTYtNTRjYi00OGExLWE2YzgtOGRmYjAxZTU3NzBiXkEyXkFqcGdeQXVyMzQ0MzA0NTM@._V1_FMjpg_UX1000_.jpg",
    },
    {
      title: "The Batman",
      year: "2022",
      rated: "18",
      runtime: "180 min",
      genre: ['action', 'noir', 'thriller'],
      poster: "https://m.media-amazon.com/images/M/MV5BOGE2NWUwMDItMjA4Yi00N2Y3LWJjMzEtMDJjZTMzZTdlZGE5XkEyXkFqcGdeQXVyODk4OTc3MTY@._V1_.jpg",
    },
    {
      title: "Texas Chainsaw Massacre",
      year: "2022",
      rated: "18",
      runtime: "90 min",
      genre: ['horror'],
      poster: "https://m.media-amazon.com/images/M/MV5BNjVhZTkxMzgtM2M1NS00NjJkLTllYjUtMzQ5Y2IxNmE4OTFlXkEyXkFqcGdeQXVyMTEyMjM2NDc2._V1_.jpg",
    },
    {
      title: "James Bond: No Time To Die",
      year: "2021",
      rated: "12A",
      runtime: "163 min",
      genre: ['action'],
      poster: "https://static.posters.cz/image/1300/james-bond-no-time-to-die-azure-teaser-i84058.jpg",
    },
    {
      title: "The Boys: Season One",
      year: "2019",
      rated: "18",
      runtime: "60 min",
      genre: ['drama'],
      poster: "https://m.media-amazon.com/images/M/MV5BNGEyOGJiNWEtMTgwMi00ODU4LTlkMjItZWI4NjFmMzgxZGY2XkEyXkFqcGdeQXVyNjcyNjcyMzQ@._V1_.jpg",
    },
    {
      title: "Bojack Horseman",
      year: "2014",
      rated: "18",
      runtime: "25 min",
      genre: ['comedy'],
      poster: "https://resizing.flixster.com/cWZ5-uNNHt23M-c7t-fei9gm9Bg=/ems.ZW1zLXByZC1hc3NldHMvdHZzZWFzb24vUlRUVjIwODUyNS53ZWJw",
    },
    {
      title: "Hereditary",
      year: "2018",
      rated: "15",
      runtime: "127 min",
      genre: ['horror'],
      poster: "https://m.media-amazon.com/images/M/MV5BOTU5MDg3OGItZWQ1Ny00ZGVmLTg2YTUtMzBkYzQ1YWIwZjlhXkEyXkFqcGdeQXVyNTAzMTY4MDA@._V1_FMjpg_UX1000_.jpg",
    },
    {
      title: "Dune: Part One",
      year: "2021",
      rated: "12A",
      runtime: "155 min",
      genre: ['sci-fi'],
      poster: "https://m.media-amazon.com/images/M/MV5BN2FjNmEyNWMtYzM0ZS00NjIyLTg5YzYtYThlMGVjNzE1OGViXkEyXkFqcGdeQXVyMTkxNjUyNQ@@._V1_FMjpg_UX1000_.jpg",
    },
    {
      title: "The Mandalorian",
      year: "2019",
      rated: "PG",
      runtime: "40 min",
      genre: ['fantasy'],
      poster: "https://m.media-amazon.com/images/M/MV5BZDhlMzY0ZGItZTcyNS00ZTAxLWIyMmYtZGQ2ODg5OWZiYmJkXkEyXkFqcGdeQXVyODkzNTgxMDg@._V1_.jpg",
    },
    {
      title: "Stranger Things",
      year: "2022",
      rated: "PG",
      runtime: "60 min",
      genre: ['Horror'],
      poster: "https://assets-prd.ignimgs.com/2022/05/12/stranger-things-4-poster-1652364986162.jpeg"
    },
    {
      title: "Hustle",
      year: "2022",
      rated: "PG",
      runtime: "90 min",
      genre: ['Drama'],
      poster: "https://occ-0-999-3212.1.nflxso.net/dnm/api/v6/X194eJsgWBDE2aQbaNdmCXGUP-Y/AAAABYzbMfJAxXAv_X_znhgRyWSMn0nE6rqlqFo_ewl0uncAiqyU0flpsBYoHQsL0Y8o7N9L45yNowV_iMrSTTRIrMswGq-z4025saX06R5ABJzKqKYUdiByrlM1_9uhA0Gvip_BUA.jpg?r=a60"
    },
    {
      title: "The Ritual",
      year: "2017",
      rated: "15",
      runtime: "94 min",
      genre: ['Horror'],
      poster: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRHTQ4gG0rqsFRQp41nBjj_iOfv9ucP8WyHFg&usqp=CAU"
    },
    {
      title: "Fantastic Beasts",
      year: "2022",
      rated: "12A",
      runtime: "143 min",
      genre: ['Fantasy'],
      poster: "data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wCEAAoHCBYVFRgWFhYZGRgYHBwaGhwcHBoaHBwYGRgaGhoYGBocIS4lHB4rIRoYJjgmKy8xNTU1GiQ7QDs0Py40NTEBDAwMEA8QHxISHzQrJSs2NDQ0NjQ0NDQ0NDo0NDQ0NDQ0NDQ0NDQ0NDQ2NDQ0NDQ0NDQ0NDU0NDQ0NDQ0NDQ0NP/AABEIAMMBAwMBIgACEQEDEQH/xAAbAAACAwEBAQAAAAAAAAAAAAAEBQIDBgABB//EAD4QAAIBAgQDBQYDBwQDAAMAAAECEQADBBIhMQVBUSJhcYGRBhMyobHBQtHwBxRSYoKS4SNyovEVssIzROL/xAAZAQADAQEBAAAAAAAAAAAAAAABAgMABAX/xAAnEQADAAICAgEEAgMBAAAAAAAAAQIDERIhMUFRBBMicWGBFJGhMv/aAAwDAQACEQMRAD8A+SA1IVWKmDTEWTFSFRr0GiIyxRU/d1Wpq9HrCVtFeSq2SjdK9yiNaOheeheUqISjHQcqqy0uh1RQVqa1PLXoSiZ0SUV7FeqtTyGsI2VxNRy1cErslYHIpyVFkotUrwpNbRuYFFTUVcbVei1WGdIGZarK0WUqJt0NBVFAWpBKsRZJHT8hRAtRRNVaKlSuy1eErmWtonyKGWoxVpqIFYZMjkrxkq4V5E0TcgcrUSKK93VLrQGVbK4rqllrqwdlGWuC1YqmiLVqaGgutA+WuiizarjYo6E5ooC1NVqYSrFSjoDorAqQE0QtqpCwaxN2irJpUfdUYbcAk7DWisNgiyg8iAfUVnoVU34FIs1auHp5b4O3SjLXCSOVI7lB42/RnVwh6URbwB6VrMPw2IEbmPkT9qNPC4UiNTU6zyii+np+WYl+H9KAe1FwLzj5nX7V9Ew/CJO1YDibKMY5/Ct2D4IwUn/iaMZeT0g/YcrbZcMGelAR/qFerAeZ0j1itnx10w5VDu2RxAmVDjP/AMR86ymHuq2IDDZrqt5G5t47jyplk2tmWHi9Nl//AI9ulUthiOVfVLfBk927ONY7PeazOI4dqdKnP1CYa+lpeGYxrVQNqASeWtae9w4dKF4lw4rZd40CkzVeaJKL3oyxfLcJ6Eemxp+uBLAMuoIkGswBr+uRrT+y3EwpNptoJHqdvU+lZtpbRW8fLRU+CZd1ih2s1syiOpyxSLH4QgmNK03vo56lz2mIbluqitMLluKFdacM3sompA1L3deERWH2jhXkV6TUZrGJZK6pQa8om2cqiiLaCg0NE2TW2JaYT7nnUjbEUTZUFdN6Is21jUb+tHZDkxUcNXnua01jhyMAfXeT+VecQ4TDf6YJUjboemtJ9yd6KNXx5GeS1TfCYYHlXq4BhGZSPlRjBbaFzsonx6DzOnnQqlroGNU3toRe0bhItr0DN5/Cv39K1XshhVu4VGO65lP9LED5Za+fX7pdmdtSxJP66Vs/2eYg5Ltvo6t/esaf2VLKmpO3HrejSrhY7hV3DrKPbRwfjUOPBhm+9L/bDH+6wxAMNcOQdYIlz/bI8WFX+wzF8Jb55CyH+ljA/tK1zNPhy/k6FS5cS282W/h0G7m439iR/wDdNrmF2mkV583E7CDZFdf6mS5I/wCArarh5EEUlT4/Q0vyZ/iWLXDWHusNFgab9pgmnfrNfFcm5Op5+M7mvsP7TLI/c0ykw11AQI1GS4wnzA9K+ZiwNo5V0YUpnsllTb0gjj7ZkwgEQMKkePvLikeRQjyoPC4cq6PqfgPmCPTamP7nnCDWEWAJ5Fmc/wDJ2PnTXAcMDlAZAzKDG8FgDHfBrVmmVopH09W9n0LEM+UrOmx7/Gk97C1o+LpFq4wGoRiPHKY+dCCznRXGzKG9RNcHJydXDa2Zz9zEyRNJvbW5kwrhB8RVW/2k6x37VumwkLm/7rC+3gIwx/mZB883/wA1XFfKlslcKU2j51YWQPEj5T9qswLRcRv5tYnqJ+RNQsjsnuJ+leTOkn59K9JeDifln0LAKcw025/nR+JwQadvtVXs/bL2lePiVTz1Ma0ZiMOTy/KuZ1+RlGp7MjisNBI6UC6RyrXvgFjXUn5Ulx+HA0UTH06d9dM2n0cdY3PYhuCh2o+5bPOg3SnDFFFTUVxr0VihZmrqhmFdWF0VpRFoVRao2ytZAt6DMHbJOlaLC4R4zMhI6jXWk+BtncDatFgMWVEHapZaa8C4pT7YXhuF5ocSvWYI8unnU2Rl0kelX4bFjw+9W8SxdvIXcZcsSeWpgepIrkbp12d0xKXRXbYEQyzWN9t8TlZbSg/xPppJ1VJ5wCD5rW1wKBrSPPxKrR0zAGPnWD9tsS7YkoRC21ULrM5gGJAG2/ypsX/oORfiZqes1r/2Z9rEug1z2580ZfszVk2JG8Vs/wBlGGDY4tBBt23fpqSqa9RDt5gV05NOWicbTRb7QYa5jL7oiFRakKXICwocuxiSGYqAB/LrB0pj+zG+ytcw7CN7upggjIjadIymlWKsXRiMQReCsHu5ik5T22kdwNF+yfEFspisx7b2sluBzadZ2AHZO+tRb/Hj6LRG637Jez93NjEva9u8W10//IWET4PX162RXy3hSKEtwRIeR4qFiK+p4ogWnYfwMfkTUMeTbf8AB15MXFJr2YP23Bu4HClfxZHIjU/6J+mY+tfPFsMCdDpvy9K3GJwqxqXyrIAloUE7DpOunOg7XDbZ1DGD3cvM1H/K/gr/AI2/DAcNgyFQkHXN8mgjx0+dPuEYBi6jYZl/9hTB8FbCopeMrXdI1EuNCOW1POE2UBEGYIO1cz5XkS2dcVOPG+u+wnjOFLWWAG8DyLCao4NhSbIX+ElfEAyPrHlTjE3VymTypNh+L2bCsGY/ETsTyHTwrruYWVbfWvk5J5VjaS72Ff8AjJ+LbpNfOfbxrd3A3WVQGs4gpO+qXig/4Op862d722winVm/t/zXzbF8Tw7W8bbJcribhupoOw3vM/a17k2namlSqTknWOtPl1+zCYYSWB59Pn9a9OXTQ8vmYFMsPh7ecgMdR086JXhikHX68jI+dd80tHnXj1Xn/psvY64WwaAbozr3/EWE+TCmz4M/iMHpzil/7P0TJdQ6wUcf1qQTH9ArQ4m1J0rjt6p6Kz3K2JL+GjQxp6+RpHjMNFbE4TmfShMTYD6EDT1p4yaJXj5I+e4u2ZM0tupW24lgl6Cs3i8KBXZNqkcbhwxIy1A0ZcShXFMPNbKq6vZrygOW2hRdpKqt26Pw1g1t6IW99INwbkcyKZ2AetUYTDd1NLGHqV0imOdeSeHtmlPttey4cKTBdxpO4UEn55flTrHXxh7L3SM2QCBtJLBQPnWB4vxBsS5doECFX+FdR85k/wDVShOnv4OnaSPp3C7Z92mkdhNOnZGlfPvaV82JvHo+X+yF/wDmtPw722w6yHW4FBUIMqmECKNYbec3kRWQv3s7M+UnM5bY/iJMfOtilqm6QMtpykgG+PhHQR8yep693h13f7P+IphcJi78oboyhFZgC2VZAicxEvy6Vh8Q2p05n9TtVmFwZPT1FdFJNaJxTXZtrmKDDENIGcZgBJ7TOzMoPgx18aRYFCXJHedht4b9O6ocZ4j7gNb5tlYyNCoUQPGZP5TUTwDEvh/fdoJAYrDBt+agzqNYmBp4Dkda/s9HHhdd7NZbvKtmyBEksTrr+Eaj+k03OIcrlZmgCIkkd0921fPOD8VLgI0jJsd99+0e+PnWrTFKS0OcukDtHNtIPz9K5cmHvZ2RkaXENx8yyiSpM+f6FQwrIoh2VZ/iIBMjYT5UPxPHBbLsD8KuRyjTQ6/4rN+xa4a5riCuZ20DOVM8gokST3b1NYnUt/A6rtI+hcLwuYZi33nXrTpbiosA61jMfjbWHVb2GYZFYK6oZQoTlYkbZlJ3GoI10o2/xLTQmua1UF5h29DTHcS03/U/9Vl+K8QBmCSOuv286qxnER1/XrWfx2OzH9coA+VNhxu3tlcjnDPXkhj7ob4M0QJn+LKM3lMx3UpxRkkqCFkxO8GYHoRVl7EmdB9PLlQmIxTH0jlsBFexjnSPCz26ezy00OpAgSB6yJo+4vaQ66NrE6TvSnOZk7fLu1q799IGgjXp/muha0cF8mzffs9uRiGQHR0YR/Mjgj5TX0B7Jr4NgeMXLLi5abI6zBCidRB0MjUEimFz20x7b321/lQc5/h8vCoZMXJ7RWHpaZ9jVF1n9eNAC6l5A9p1ZDsVOhI3mOlfIm9qMa3/AOy/PoN/AUV7I8Ze3iLaO590xZChaEBcdkxsO0FHhNJ9hpb2PyN1j7A1rK4+wZrZXiDrv9KzvFcSi7nU8udUxtrwc2XTXZlryUHcFGX8QDJAI7qBvPXSRhMpiuqv3gr2gdGmNQWGwnw1pzhrIGVw+hGob005g0ksBpkMB5gfKi1XnMzzpK7Iyteh3e4oiJ2YL9OQ7z1qhPaVkBzoGmcuXSCOR30pHiFgaHXn60Lk2La0nGdFJmm9s0XE+OLesrbCsGlC0xl7AkgGZOsbgUkwuFJmcuxiImTUVQDl159d6ssAd/nWS0uiySXkMGCXKdJ79N58KZDCkBdttjy/h3+dAWSACM06c9TpqPqaOXGtl1A1569Z61OqrZSYlJi3HYMZzGskDTvOtP7HC0RcxRQRG41mfl40qwrTmYiSDm3iNY1HSjk4wxRgwnlpzGsiPTWhbppJD4plNtoH43luI2bXKxZSohgQPwknRq1Ps/atG1ZvI9xmFtFce9bKz5RmZreYgazoQKwHF8SWU2yxBI1bnz37jz2on2b40yqtu6yqiFVygNndTzzTAA7OggmRS3FOOjqwWpp8hlj7dhLot20yMBmYlh2s8EZSPwgAQDrqdBzMs2SNCN9taQ+1mNs3MQl2zmyMqo+mUllY5sup/CwXlqlaH2f4kt9nzFE1C20kZoG5k/FuBp0pLmphP/Y03NZH/wAL8ZgTds3EGjMrBZ0GYjsyekxWV9nMcLVprYsD94V0CntSwS5mdTAOUgKykgcxX0TFXbVhQ124iA7ZmCz/ALQdT5V8o4pxWz+9XntjNbZswMbkqM5ykbFsx160mDdJrXXke7U0n/R9CxnELF2yFa0tu5cdFuKR2pzKxBBGo7WnjULriKzPDLbMoxeQrZRgiZjGdySOx3KobXbYcjDk4xHnIZ6jmPGofUY2mkdOHOntoDxTjXnSTEuSdNPGmuIYnlS+6pq2CUkc2fK6YtdDVZSjXtCag1oV2zo4a2CmzUWWKNS0RXtyzPjVJaOe5bF1UMhmjrlqKqyVTiST0CNIqsEzPKjGAqspSuSis8tYx0MozIf5SVPy3o9eLswhgSebaGT1128u+lzJVJQ0PAWppdjVmB2IOn60qi4aCt22Yws/SPOjUt5Rq2Y/raty+RHCn2Ve5NdVkDv9a6jyNthSUQb0ADnQIuxtUXukmhQkS97DS86evfUkXM2g0G9A2mMxTLDAbcuZpK6OqZ2ehZ2FVlh4a0yv2UyI6vLNIKa9kcj3zr6a0Lbw8mlb15HUbOw4LaCSTsACSfSmXuwNGUjbQgg6CBvVHCrgGLt2QUWCp7ZIDMRmgwNQNIB0kVqvak5v3e4FUe8JXKFZW+EnM6MJBBUieYPhXNdPl46OqcK4732Z1MIeWk0LxQlEAXQlonmYUnT0rRYexpFZj2xxK+892p+BTMcnbcHrACfOmw07vRskKJ2I1aVk8+0fE60y4Xj2w2JLqAcoVGHWUUOs8jmBg8iBQ2Aw+RfePsozBfDUFu7u50Jg74YHNu0k+J3NdN6fSOeNrtm3/ahfRzhXtxldS8jSQ8BSe/T5VkA2gHf4cyahiy7Llz5gg7IJ2VS9wgeZYz314jS6qNyunmRvWx9Q0ClukwkcIfEszZ2LAElnM5mjsrJ+vIULY4Myi257QcO0clyLJDE6blfnTv8AeBbtsBtok/7zDN5LmPdFCYi0zFAs57d2QJjsPEnwBTX/AHUibX6KvTNX7XcSGIwOGVE9yyFHdMhT3bgG0EVTELLsR3Zax2EZ0AliWHOTqOVEe0N+7cDsrkqpAcD8QWDPgrTp0A6UFhsTmXNzG/6+dCp5LsCfF9D3DYtn+LYad560Rdw88hSDDYkDn5Dc1teBupRXZA8HKQZj4gNY7iK5ang18HRLVr+RPwjgdzFO623QZDBZiTDcwFA18SaAxuCuWb72LgXOoDAqTlZT+IT9D3024M1uziLyDMXN8qVV2VfdOjHTKw7YPfuvKtDxTh1n3udMzNlVCWJZgFzESWkk9rXwFNV8GN9pVPRiVB2rx7Ws0y9oE/d0NwDchR3EzrHlVPsrgVvo7XkNwvIQhwrBwpIC6yDoZB0Om/Jvu/jzXgl/jtvi/IBctaaig3txyp9wm2biMH1a2zIx71O+lAoj3Q/u7TuEbKSqlyDJ/CuvLlMVac/lEb+l3piV1qpqcHhzhmRwbbKcrKwMgwD56EetceGpzJPyHy/OuhZZ0cjxuXoSEE6DfuolMEd29PzNP+E8Le6/u7KDNBMcyBqdTQOISCQdwYpKtvwgAjmBAGn63oZ++iGqsgVkvkQozH9f911e5a6m2E60KkLetSVIq60lT5HTMaJImkAUTb6DavbNmi+GcPa/eNpXW3lXPmZS5Op0CjuU1N0i0w20kRRO0B/K3yK/nTTB4WSJoa7iTh3/ANQA/EgELlzqTrLjNkYRsQdpnkLxnEh7Ft1aCrw6gwZKsVMc17Onj41F7rWvZdSp7flEuP2U96jWcvvVMsWIVCANAc0KxA31mCBBnRj/AOTKG0b6oVthiq2lKLnyhcxzSWIBI5b7UlwrRBMyJiJIkxv4R6TRaWVKkCJ5Ttsdx6etHj1pjOl5Xs0WH9prGrMhChC0zJzAAqhAH4tgfDrp86QtduFn3Zmd+mpk+pMVPEEglNtSCN+ny2irsHCIWI3MeQG/qTXRiwrFLpeWc2XJzpT8EeMYnsZQfiIk92/2pdhVIGwPm320r3iBllA33+eny+tcllxsv/r+dNPSFYcrmYESUYDKdJNq4By8oqvAPDXHO6rlXnBbQVy5iNQQR3lTEawR5fOqcJJZhrBZSZ3IAY/WPSj8mC8biwqhD1k+ER9zRPDeJKpncgZQx3IGsTz6eQ8aQ4m5mcnQdD3cqKx2HRbasPiOXWSdxJHSg5WtG2NMNj+x094zEnpmJkD1pJZfKTGkjKw7xpPr9TTTErCJHwgL9AQfH86U41MrnoYI+n51kkbYyR5AMkaCI3NGrxS5aWEuPBOuWPGY2nTcRsKR4e+Yyx4f5HOmeGxQRXLANKsAGAYhiI7JYEroTtBpalNeNjw9PyWcMYLdF1LtxW1zFGyuZBJAZupiTr1g1qfaMnDLh8RYzKLtpWdHJfMwYlnYmJ+Ne1od6wWEv5HVhyInz3NaHFY13trbZpW2GVAeWZ8xmNwTS3K32Um9rroc4jitjEWGTKzM4jKYUqw2YE6Eg6iPOlfCLNzDFibiqpACkkgkkgSF2JE8yPGszdlFkGNiPpB79flU8Dh3vsAXIWYnUwTEaelSWHin30VnLya67N9h+K4XCWzbEsSFcahnf3kkFjovwqp3/EKB4NjrFvE5rD3ba3Ul2Zrci72mKjMjLlk6aT9KzfFLT2wmYzllROURljkI/iBk6nMdd6WtjT0qmLFDl9+SOW6nItLx6Nz7T45FusWLBjBKsczyVEhgDC66RMaaUHbx9tbj28puEIDK9tQ7FCVyhlmAWUnOu2nQ5rh2Cu4q5lU6kFmLH8IIBPUnUVs8N7OC0j5WdrjrBY9YMZRy1jcnxoVxhab7Ak7p1oAtOyOzocp1+E/CDPZGpI001JPeaEuAkknemuBvLetW7asQyfhlCcoEOGCiVOY6TAgCvL+DidKVZX4YmTAk9z2JGFU3Ejxpk9iqGs606s53iF/6511GZBXU3IHAGVJoyzaqFm3TCwIO1RqjrmArA4UzrV1+0VvWPd63LjhcucoCFLFWLAHKFY8tTmjWr8L2o6frasYOIOS9wntPI8AQQANNguYeffSY5dU38F6aiUbPE8Zwz3Xt3WDqpy5yoKNGrGAOyM5eDtGs61kfaLDJau5bb50gMms5VbtZc34txr0igs0R31XjFgAjpr3bAV0TjUvaf9EayOl2EYTHcjyPrJ/zTpVeYB8j9qzWEgMOzm2JJ+EeXPzovEcXOUKohgBLd43yj709S34ETPcRdzO2kQcpnmRIJ+leYdHuEIswu8cyTt86b+zvBUuWXu3nIGsEMNNCxZiQeh36CltnjotoUW0h0IzEtqYjNHLXWKZ5FU8V6B9ty+T9gdkAuxG2aB4LoD9KaTptSfhqyaKxHEVGiiT1O3+aDQNlmJfU+AH3+9V2XgFttIHidPzptwDgjYi3cvXAwQI+QiFBdVnc8pgVnsxZRGwrS020vQ1S5Sb9g10jMY2pheM2o02Uj+0T56fM0tUTJ/WtG5soAEGB07qZiDW0nvLK5SAQBrG8CDPpQPEbTFZMSu/gdNOomruC3pVk5jUeB/I/WrOKMQm3xkLPzP0pfYQHBLG25176uxNssvZGszFRw6HealmOYEQY5UTAeFt5mg7bmmiOefj/ANVQ6CSwBE7jofyr0OO/b9a7c6RvZSejkQMGWdiR/S2vyn5VDhN97ZaFnXXy3j0qm1fy3T0P5CjMIwzwZE9K1Lpj43+a0WcX4mcQM2XLBHzBB9YHpSJ1g0yuMolTtO+xlTH3O9ccA7KSql1Akle0QDMMwElRod+ho40kteAZtut+fkd/s+XNiV/lR58Oz9yKa+0PtFmd7VsQFYozc2IMEL0Xcd9Cfsz0uXifhFuSekMvPloD6d1Z+65Z2cjVgWI7y0kfOpOVeV79JAVOYWvex7hsYVtNkCpORlyqogqGQ8ucmZmTvNMOGY83wyuBmUTI5iY25EaetZdbs28s6hj3aAGP/YelMPZ27lvD+dcvqJ+q0MsJy37GivyS9DXE2wCaXXBTrFgUuuoKhFdDZI0wOuqzJXVTkR4llpVFFJbBOnOllt6YYc85pKTReaT6DpKI7H8Cs39qk/avnltjt0A/XyrXe0uNyWMk63CF/pEFj9B51jrXPwFX+nl8W37J567S+C530FMOJKBbkwGhRHM/iMDxI9KCt4Z3DMqMyoMzkAkKNgWjYb+lN8ZbUYZmCiWA1jWCwjXw5U2R6a/ZsUtp/oS20AWT+gBQgBY99NuF20dSrjzmCKquYcI/YZo8YbyNX5LwQ17L8Bi3SzcQHstIjXd1ysdDroOciRSe4IMVoFwqNYZ/ef6mcDIRBgBu14ais6zSZrcdd/IFfLr4CbRIUjbN9NophxHg3u7Nu7nVhcBIAMsIMQ45Hp1pdiz2iBsunppUHxDEAEmBTppJpoVqm00zWWvawDCtaYAn3YtIgUiAAAXZ80GdWgLvl1gVlLt8nQaDkKorqkpS8Fqp1rfo9U0QraVQo0rlMUWIH4FGDBl3+oPKtHb4Z+8lAWyKSQDGpcCWJnYKPm1I8A2grQ8ExGUsWbMVXIJAgCczkAQBLEA8zEak1K20torhSdaoVcUwRw7MhIJVcwIESpmDHLUERWeW4QZBg0+9oOK2rjuVUsYyqxOw3JEb9onWs9TzvXYtpKnx8DTD8UEQ6yOo39DUlKt8DSOmubzB+00pq4ICJBg9D+fKi5Qu9EsQIY+RHpT3hfui0uJIU5ddpU6xIM7Eb7ERrIRM2YGfiUeoG4PePzqNi6VIIoVO1oeKSrbDOKCLpnUMAdfCPtUcNcywVOVg2YNpIYbEHfy2qzHWmeHAOWAJjQGdAem9AqSppoaa0zZVSbpH0L2XyjCcRugqHYP2RHZX3bMkDkJZgP8Ab3VmL57CDmTc8xktZfnnqHDsWVzAbXFa04kCQ4gb6aNlPlV/FsPkuqsMsWwSrTKsWMxIHQGpueNv+ewKuU7+AO0NG8/tVmGu5HRh+GG/tM/nVVo6NTDgWHR2IZSxCmANNzBYmRtINGmkm2aVukkae+00BdNHXFAETt+taX3TXDMnVdFDCuqM11U0Q2L7L0xw96KR27sUbZvVZxsmq0H8aw/v1RRAIeJicoYb+EhfWsneGR2TfKxWdpykjatfgmZ2CqJOungJrN4tJZx1c/8AJ/8ANNjTla9GqlX7COD8RdFdEAXPozSRodNY33OlM8dhitk2pzFezIEd4MTpuKT2TAg7qSvjBptj8Xl7W85Tp+u6lyrtNfJbDk8p/GhDw1oZga64/bienrUbTgPsdWbQ7wYImhi3aJPU1byznZpXwy3AoGj7BhofM9KGuey7T2biEfzZlPoAfrXYS/AB6EEfWnAxFS3S8DJz7M7e4QytldgJBIYHMCRl8P4vlQ9zhjgSIb5H5024rczlZ5aep/8A5FQtEgfeqJvXYjffQhuWmXcETqJESOo6ioLWv4yS9gIihiCscyAOnyrKZPXp9/10oy9+QvXolZqmdaltNQFEyG2CMRTVlUrECTr016nw60nwtHkFlIG5Uj5UrBsV3uF3U/DPeNaFa0w3UjxBrScJx4ICPuNAT9D0Io3EWR4g0dm2YquBpxe4YuYgNln4Z1E7QeYpZiLDIxVhqP1pR2FPZBGgg0QuG1359KFphaYMygzI8tCB0oU9Dyk32OcHfW3bKHVT1213BNJ8VbVjKnw5x3HrTPEYkWGZdwVHIHQnUa6cjv1pVnLnKuiiST0AEk1OE97Xs6ctripfo8w+kg68j506xV/31xndwrratkAg9tiqyBGxIYNr0NJcMuYhR+IgeEmjMcwOIYjYFQPAKo+1Xeuto4k33roqtnfx/X1pj7P3st3xzL8p+1L1Hxf7vsBVvD3hgeh/xUqW00GXp7NZiLwNA3LndQz4mqXeajMaGrI2WG5XUNNdT8BOYnR6uS8aEBr0tVQDK3io50L73tk/zKf+Qodnr0fCfWsYv95DseTEnzJppav9le4Dy0ik9szVguUGYvxyAktz3PlpIPIxQdm0pBnXpy6mrGuVUDvrQD6G/Cgot3QVByiQSJI0MQeXKpYa7MLqfqYFCYQxZud8DyABNCW7zDYkecUqXbKV62NMQ+Y/CFII0knmddamADFLMC3bMk9qd95B/wC6KD6RTCPyX4ssinv0BB0/wYnekoUCiRcLMFnQfMifzqgr1oroFJb6JY1RlVuf25UEKIvXJEUON6ZGXgPw13WIpij7Hu+opLaENB604TalZmUYu3m7a/EN/LY+NEcM4ixZUbWe/uoC3fqVy7ABAEjTyJom0NuI4jLl7MkmAI36/rvoDjBVgp3cdP4ehH650M5MCS2mg10APIVyrG3PT1ob0ZIrwvD2cTIA9T6Ufdw6qAwEtK6ye4bbVXYu5VA8frUmu5onqPlr9qDfQVvkijG3TcuZe/T01NWuotW31lm7M9x5DymhnaGzDwPhtXYq5mI02H1P+KK6SRqbdbJcO+MHoCft968xFwi4xiSTNdZuqOQHh0768a4Jnr3a6UW9i6aZNC/a0jcgd8jT6+lTwTtvlEHxHpvNQ/ex0NV27xGkGgw9jP3nfUDdoVWmptQ0hdE85rqr9K6j0LxAa6urqJU8avSd66urDI5Kmte11KY9G9Vrzrq6sAaWbY9w5jWfypYa9rqE+WNXhErHxCi35+ddXUzJ+wTD/EKIxXwmurqzC/IDVb11dRRiafEP1ypom3pXtdQYGLBVp2rq6sxyd3avENdXUvoKLDUOddXVjHgqS15XURSWQTtVbb11dWQDjXldXVjE0r2a6urGPa8rq6sKf//Z"
    },
    {
      title: "The Shawshank Redemption",
      year: "1997",
      rated: "15",
      runtime: "142 min",
      genre: ['Drama'],
      poster: "https://media.vanityfair.com/photos/5d8535de6879fa00082e6ed9/master/pass/the-Shawshank-Redemption-movie-lede.png"
    },
    {
      title: "Rick and Morty",
      year: "2013",
      rated: "15",
      runtime: "30 mins",
      genre: ['Sitcom'],
      poster: "https://flxt.tmsimg.com/assets/p10376284_b_h9_av.jpg"
    },
    {
      title: "Midnight Mass",
      year: "2021",
      rated: "18",
      runtime: "60 mins",
      genre: ['Horror'],
      poster: "https://images.squarespace-cdn.com/content/v1/5fe76a518d20536a3fbd7246/1634156523618-MPCU0389M80DS2AE1CC3/p20481773_b_h8_ab.jpeg?format=1500w"
    }
  ]
  })
}
</script>

<style lang="scss">
@import 'assets/scss/_color-palette.scss';
 body {
  margin: 0 !important;
  padding: 0 !important;
  box-sizing: border-box !important;
}

// .movies-container {
//   display: grid;
//   grid-template-rows: 300px 300px 300px;
//   grid-template-columns: 450px 450px 450px;
// }

.movies-container {
  display: grid;
  grid-template-columns: repeat(4,150px);  /* 3 columns */
  grid-template-rows: repeat(4,150px); /* 3 rows  */
  grid-gap:100px 300px; /* 50 pixels of space added between rows and 30 pixels added between columns  */
}

.homepage-container {
  // background-color: colorPaletteSetting(primary);
  background-color: #0d0f19;
  display: flex;
  // justify-content: space-evenly;
  height: 100vh;
}
</style>
