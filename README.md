Здравствуйте, нужна ваша помощь
1) ВОПРОС
 // В строке 20 выдает ошибку,что string[] и string несовместимы, но когда я меняю allId: any - все работет
...


interface FilteredInfo {
  allId: string[];
}

const normalizeData = (unnormalizedData: testData[]) => {
  const filteredObject: FilteredInfo = {
    allId: [],
  };



  let data = unnormalizedData.map((el) => el.id);

  if (Array.isArray(filteredObject.allId)) {
    filteredObject.allId.push(data);            
  }
  ...


  2) ВОПРОС
Получаю объект + массив + массив
Можно как-то убрать один массив

{
  allId: [
    [
      '62e69d5a5458aac0ed320b35',
      '62e69d5a5458aac0ed320b1c',
      '62e69d5a5458aac0ed320b32',
      '62e69d5a5458aac0ed320b39',
      '62e69d5a5458aac0ed320b53',
      '62e69d5a5458aac0ed320b19',
      '62e69d5a5458aac0ed320b25'
    ]
  ]
}



3) ВОПРОС
Можете подсказать в каком направлении двигаться дальше, чтобы отфильтровать вот так

byId: {
 *      62e69d5a5458aac0ed320b35: { id: '...', title: '...', body: '...' },
 *      62e69d5a5458aac0ed320b1c: { id: '...', title: '...', body: '...' },
 *      ...
 *    },

