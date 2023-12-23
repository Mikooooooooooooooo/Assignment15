<template>
  <div class="container">

    
    <text-input></text-input>
    <email-input></email-input>
    <password-input></password-input>
    <message-box message="Aren't you something to admire , cause your shine is something like a mirror"> 
      <button-buttons title="Open Message"></button-buttons>
    </message-box>
    <number-input></number-input>
    <file-input title="Custom Input"></file-input>
    <date-input></date-input>
    <form-textarea></form-textarea>
    <form-select title="Who is Aimat" :arr="['cdsjbcs' , 'cshbcdsj' ,'csdcscbsd']"></form-select>
    <form-checkbox title="Whcskjsdkc" :items="['cdhjbdc' , 'cjscds' , 'csdkjncdsk']"></form-checkbox>
    <form-checkbox title="cdjsckjs" :items="courses"></form-checkbox>
    <form-radiobox title="CDijcbdbsd" :items="['cdscs' , 'cbgnkn' , 'dfnekvrn']"></form-radiobox>
    <form-toggles></form-toggles>
    <button-buttons title="Click"></button-buttons>
    <dropdawn-buttons title="DropDawn" :links="links"></dropdawn-buttons>
    <group-buttons :buttons="buttons"></group-buttons>
    <sliders value="20"></sliders>
    <forms :items="['Name' , 'Surname' ]"> </forms>
    <input-groups title="name"></input-groups>
    <card option="December 21" title="MAT 254" text="Solve problems from sample final , repeat formulas , working with your previous mistakes in quizzes|midterms discuss about the final with your friends"> </card> 
    <accordion title="Text1" text="My name is Miras . I am 18 years old . I was born in Karaganda region , but leaving in Kaskelen city , cause my univer is placed here." > </accordion>
    <collapse title="Text1" text="My name is Miras . I am 18 years old . I was born in Karaganda region , but leaving in Kaskelen city , cause my univer is placed here." > </collapse>
    <badges title="Bucket" count="5"> </badges>
    <progress-bar height="20" percent="50"> </progress-bar>
    <tooltip message="To all the things I've lost on you"><h1>Miras</h1></tooltip>
    <modal-window message="Aren't you something to admire , cause your shine is something like a mirror"> 
      <button-buttons title="Open Message"></button-buttons>
    </modal-window>
    <alert message="Aren't you something to admire , cause your shine is something like a mirror"> 
      <button-buttons title="Open Message"></button-buttons>
    </alert>
    <icons iconType="icon"> </icons>
    <image-carousel :sources="sources"> </image-carousel>
    <tables :grid="table"> </tables>
    <list title="Hello World" :items="listItems" />
    <page-header title="Sammeramena e e e" :links="headerLinks" />
    <page-footers  :links="footerLinks" />
    <br>
    <page-slidebar :title="sidebarTitle" :menu-items="sidebarMenuItems" />
    <search-bars/>
    <breadcrumb :items="breadcrumbItems" />
    <pagination current="1" max="15"/>
    <tags>Tag</tags>
    <list-group :items="arr" />
    <navigation-links :links="breadcrumbItems"  />
    <br/>
    <link-groups :linkGroups="LinkGroupsItems"></link-groups>
    <navbar :title="sidebarTitle" :menu-items="sidebarMenuItems" />
    <tabs :tabs="TabsList">
      <template v-slot:0>
        <div>
          Content for Tab 1
        </div>
      </template>
      <template v-slot:1>
        <div>
          Content for Tab 2
        </div>
      </template>
    </tabs>

    <drawers :drawers="DrawersList">
      <template v-slot:0="{ drawerIndex }">
        <p>This is the content for Drawer 0</p>
      </template>
      <template v-slot:1="{ drawerIndex }">
        <p>This is the content for Drawer 1</p>
      </template>
    </drawers>
    <spin :loading="isLoading" />
    <divider/>
    <images :source="sources[0]" />
    <texts text="No more couting dollars" variant="heading1" />
    <user-profile :user="currentUser" />
    <date-picker/>
    <grid-system :items="gridItems" :columns="3" />


 </div> 
</template>

<script>

import Text_Input from './components/input/form_input/text_input.vue'
import Email_Input from './components/input/form_input/email_input.vue' 
import Password_Input from './components/input/form_input/password_input.vue'
import Number_Input from './components/input/form_input/number__input.vue'
import File_Input from './components/input/form_input/file__input.vue'
import Date_Input from './components/input/form_input/date__input.vue'
import Form_Select from './components/input/form_select.vue'
import Form_Textarea from './components/input/form__textarea.vue'
import Form_Checkbox from './components/input/form__checkbox.vue'
import Form_RadioBox from './components/input/form__radiobox.vue'
import Form_Toggles from './components/input/form__toggles.vue'
import Button_Buttons from './components/input/buttons/buttons-button.vue'
import Dropdawn_Buttons from './components/input/buttons/buttons-dropdawn.vue'
import Group_Buttons from './components/input/group__buttons.vue'
import Sliders from './components/input/sliders.vue'
import Forms from './components/input/forms.vue'
import Input_Groups from './components/input/input__groups.vue'
import Card from './components/containers/card.vue'
import Accordion from './components/containers/accordion.vue'
import Collapse from './components/containers/collapse.vue'
import Badges from './components/content/badges.vue'
import Progress from './components/content/progress.vue'
import Tooltip from './components/content/tooltip.vue'
import Message__Box from './components/content/message__box.vue'
import Modal__Window from './components/content/modal__window.vue'
import Alert from './components/content/alert.vue'
import Icons from './components/content/icons.vue'
import Image__Carousel from './components/content/image-carousel.vue'
import Tables from './components/content/tables.vue'
import List from './components/content/List.vue'
import Page__Header from './components/content/page__header.vue'
import Page__Footers from './components/content/page__footers.vue'
import Page__Slidebar from './components/content/page__slidebar.vue'
import Search__Bars from './components/navigations/search__bars.vue'
import Breadcrumb from './components/navigations/breadcrumb.vue'
import Pagination from './components/navigations/pagination.vue'
import Tags from './components/navigations/tags.vue'
import List__Group from './components/navigations/list__group.vue'
import Navigation__Links from './components/navigations/navigation__links.vue'
import Link__Groups from  './components/navigations/link__groups.vue'
import Navbar from './components/navigations/navbar.vue'
import Tabs from './components/navigations/tabs.vue'
import Drawers from './components/navigations/drawers.vue'
import Spin from './components/other/spin.vue'
import Divider from './components/other/divider.vue'
import Image from './components/other/image.vue'
import Text from './components/other/text.vue'
import User__Profile from './components/other/user__profile.vue'
import Date__Picker from './components/other/date__picker.vue'
import Grid__System from './components/other/grid__system.vue'

export default {
 components:{
    'text-input': Text_Input,
    'email-input': Email_Input,
    'password-input': Password_Input,
    'number-input': Number_Input,
    'file-input': File_Input,
    'date-input': Date_Input,
    'form-select': Form_Select,
    'form-textarea': Form_Textarea,
    'form-checkbox': Form_Checkbox,
    'form-radiobox': Form_RadioBox,
    'form-toggles': Form_Toggles,
    'button-buttons': Button_Buttons,
    'dropdawn-buttons': Dropdawn_Buttons,
    'group-buttons': Group_Buttons,
    'sliders': Sliders,
    'forms': Forms,
    'input-groups': Input_Groups,
    'card': Card,
    'accordion': Accordion,
    'collapse': Collapse,
    'badges': Badges,
    'progress-bar': Progress,
    'tooltip': Tooltip,
    'message-box': Message__Box,
    'modal-window': Modal__Window,
    'alert': Alert,
    'icons': Icons,
    'image-carousel': Image__Carousel,
    'tables': Tables,
    'list': List,
    'page-header': Page__Header,
    'page-footers': Page__Footers,
    'page-slidebar': Page__Slidebar,
    'search-bars': Search__Bars,
    'breadcrumb': Breadcrumb,
    'pagination': Pagination,
    'tags': Tags,
    'list-group' : List__Group , 
    'navigation-links': Navigation__Links , 
    'link-groups' : Link__Groups , 
    'navbar' : Navbar , 
    'tabs' : Tabs , 
    'drawers' : Drawers , 
    'spin' : Spin , 
    'divider' : Divider , 
    'images' : Image , 
    'texts' : Text , 
    'user-profile': User__Profile , 
    'date-picker' : Date__Picker , 
    'grid-system' : Grid__System , 
  }  ,
 data() {
    return {
      username: '',
      arr: ['Miras' , 'Aimat' , 'Lashyn' , 'Daulet'] , 
      courses: ['INF 231' , 'MAT 254' , 'CSS 205' , 'MDE 133'] , 
      links: ['https://www.instagram.com/chrisheria/?hl=en' , 'https://www.youtube.com/channel/UCaBqRxHEMomgFU-AkSfodCw' , 'https://twitter.com/ChristianHeria'] , 
      buttons: ['Add' , 'Remove' , 'To Favorite'] , 
      sources: ['https://cdn.vuetifyjs.com/images/cards/hotel.jpg' , 'https://cdn.vuetifyjs.com/images/cards/sunshine.jpg' ,'https://cdn.vuetifyjs.com/images/cards/docks.jpg' ] , 
      table: [['Name' , 'Calories'] , ['Frozen Yogurt' , '139'] ,['Ice cream sandwich' , '237'] , ['Eclair' , '262'] ] , 
      listItems: [
        { id: 1, text: 'Item 1' },
        { id: 2, text: 'Item 2' },
        { id: 3, text: 'Item 3' },
      ] , 
      headerLinks: [
        { id: 1, text: 'Home', url: '#' },
        { id: 2, text: 'About', url: '#' },
        { id: 3, text: 'Contact', url: '#' },
      ],
      currentYear: new Date().getFullYear(),
      footerLinks: [
        { id: 1, text: 'Privacy Policy', url: '#' },
        { id: 2, text: 'Terms of Service', url: '#' },
        { id: 3, text: 'Contact Us', url: '#' },
      ],
      sidebarTitle: 'Navigation',
      sidebarMenuItems: [
        { id: 1, text: 'Home', route: '/' },
        { id: 2, text: 'About', route: '/about' },
        { id: 3, text: 'Contact', route: '/contact' },
      ],
      breadcrumbItems: [
        { text: 'Home', route: '/' },
        { text: 'Products', route: '/products' },
        { text: 'Category', route: '/products/category' },
        { text: 'Current Page', route: '/products/category/current' },
      ],
      totalItems: 100,
      itemsPerPage: 10,
      currentPage: 1,
      LinkGroupsItems: [
        {
          title: 'Main Links',
          links: [
            { href: '/', text: 'Home' },
            { href: '/about', text: 'About' },
            { href: '/contact', text: 'Contact' },
          ],
        },
        {
          title: 'Other Links',
          links: [
            { href: '/blog', text: 'Blog' },
            { href: '/portfolio', text: 'Portfolio' },
          ],
        },
      ],
      TabsList: [
        { title: 'Tab 1' },
        { title: 'Tab 2' },
      ],
      DrawersList: [
        { title: 'Drawer 0', open: false },
        { title: 'Drawer 1', open: false },
      ],
      isLoading: true , 
      currentUser: {
        name: 'John Doe',
        email: 'john.doe@example.com',
        image: 'https://cdn.vuetifyjs.com/images/cards/hotel.jpg'
      },
      gridItems: ['Item 1', 'Item 2', 'Item 3', 'Item 4', 'Item 5', 'Item 6', 'Item 7', 'Item 8', 'Item 9'],
      lineChartData: {
        labels: ['Label 1', 'Label 2', 'Label 3', 'Label 4'],
        datasets: [
          {
            label: 'Dataset 1',
            borderColor: 'rgba(75, 192, 192, 1)',
            borderWidth: 2,
            pointBackgroundColor: 'rgba(75, 192, 192, 1)',
            data: [65, 59, 80, 81],
          },
        ],
      },
    }
  }
}
</script>

<style> 
  *{
    border: 0 ; 
    margin: 0 ; 
  }

  .container{
    width: 85% ; 
    margin: 7vh auto ; 
  }

</style>
  